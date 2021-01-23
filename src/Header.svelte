<script lang="ts">
    import {
        Collapse,
        Navbar,
        NavbarToggler,
        NavbarBrand,
        Nav,
        NavItem,
        NavLink,
        Button,
    } from "sveltestrap";

    let isOpen = false;
    const toggle = () => (isOpen = !isOpen);
</script>

<Navbar
    color="light"
    light
    style="min-height: 80px;box-shadow: 0 2px 3px 0 rgba(0, 0, 0, 0.16);background-color: #fff;padding:0"
>
    <NavbarToggler
        on:click={toggle}
        className="mr-2"
        style="
    line-height: 70px;
    font-size: 12px;    
    padding-left: 30px;
    padding-right: 30px;
    display: inline-block;
    text-align: center;
    font-weight: 700;
    border:none;
    color: #fff;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 0;
    margin-bottom: 0;"
    />
    <NavbarBrand href="/" class="mr-auto" style="margin-left:10px"
        >Keoma Klaver Klein</NavbarBrand
    >
    <buttom class="button-2">Algumas opções</buttom>
    <Collapse {isOpen} navbar>
        <Nav navbar>
            <NavItem>
                <NavLink href="#components/">Components</NavLink>
            </NavItem>
            <NavItem>
                <NavLink href="">GitHub</NavLink>
            </NavItem>
        </Nav>
    </Collapse>
</Navbar>

<style>
    .mr-2 {
        line-height: 80px;
        font-size: 12px;
        padding-left: 30px;
        padding-right: 30px;
        display: inline-block;
        text-align: center;
        font-weight: 700;
        background-color: #ff3e00;
        color: #fff;
        text-transform: uppercase;
        text-decoration: none;
        border-radius: 0;
    }

    .button-2 {
        line-height: 80px;
        font-size: 12px;
        padding-left: 30px;
        padding-right: 30px;
        display: inline-block;
        text-align: center;
        font-weight: 700;
        background-color: #ff3e00;
        color: #fff;
        text-transform: uppercase;
        text-decoration: none;
        border-radius: 0;
        margin-bottom: 0;
    }

    .btn-secondary.focus,
    .btn-secondary:focus {
        color: #fff;
        background-color: #919;
    }
</style>
