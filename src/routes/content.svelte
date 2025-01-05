<script>
    let domain_name;
    let domain;
    let price = 0;
    let showCart = false;
    import Cart from "./cart.svelte";

    $: {
    if (domain == "com") {
        price = 222100;
    } else if (domain == "net") {
        price = 253500;
    } else if (domain == "org") {
        price = 257000;
    } else if (domain == "my.id") {
        price = 25000;
    } else if (domain == "biz.id") {
        price = 24000;
    } else {
        price = 0;
    }
}

    function toggleCart() {
        showCart = !showCart;
    }

</script>

    <div class="Content">
    <center>
        <input type="text" name="domain_name" placeholder="Masukan nama domain" bind:value={domain_name}>
        <select name="domain" bind:value={domain}>
            <!-- <option value="" disabled>Pilih top-level domain</option> -->
            <option value="com">.com</option>
            <option value="net">.net</option>
            <option value="org">.org</option>
            <option value="my.id">.my.id</option>
            <option value="biz.id">.biz.id</option>
        </select>
        <p>{domain_name}.{domain}</p>

        <p>IDR. {price} <button>Add to Cart</button> </p>
        </center>
        
        <center>
        <br>
        <h2>Paket Web Hosting</h2>
    </center>
    
    <div class="paket-hosting">
    <div class="package">
        <img src="" alt="">
        <b>Newbie</b>
        <h3>IDR. 10.000 / Bulan</h3>
        <p>
            1 Domain <br>	
            1 GB Storage <br>	
            Unlimited Bandwidth	<br>
            Unlimited Email Account	<br>
            Free Domain <br><br>
            <button>Add to Cart</button>
        </p>
    </div>

    <div class="package">
        <img src="" alt="">
        <b>Intermediate</b>
        <h3>IDR. 20.000 / Bulan</h3>
        <p>
            1 Domain <br>	
            2 GB Storage <br>	
            Unlimited Bandwidth	<br>
            Unlimited Email Account	<br>
            Free Domain <br><br>
            <button>Add to Cart</button>
        </p>
    </div>

    <div class="package">
        <img src="" alt="">
        <b>Expert</b>
        <h3>IDR. 30.000 / Bulan</h3>
        <p>
            1 Domain <br>	
            3 GB Storage <br>	
            Unlimited Bandwidth	<br>
            Unlimited Email Account	<br>
            Free Domain <br><br>
            <button>Add to Cart</button>
        </p>
    </div>

    <div class="package">
        <img src="" alt="">
        <b>Master</b>
        <h3>IDR. 40.000 / Bulan</h3>
        <p>
            1 Domain <br>	
            8 GB Storage <br>	
            Unlimited Bandwidth	<br>
            Unlimited Email Account	<br>
            Free Domain <br><br>
            <button>Add to Cart</button>
        </p>
    </div>

    </div>
</div>

<button class="Cart" on:click={toggleCart}>
    <p>Cart</p>
</button>

<div id="Cart" style="display: {showCart ? 'flex' : 'none'};">
    <div id="Cartmenu">
        <button id="closeCart" on:click={toggleCart}>
            <p>Close</p>
        </button>
        <Cart/>
    </div>
</div>
<style>
    .package {
        border: solid black 1px;
        /* width: 25%; */
        padding: 25px;
    }
    .paket-hosting {
        display: flex;
        justify-content: space-between;
        padding: 0 40px;
    }
    .Cart {
        text-decoration: none;
        position: fixed;
        /* bottom: 0; */
        right: 5px;
        border-radius: 25px;
        border: solid black 3px;
        background-color: aquamarine;
    }
    #Cart {
        top: 0;
        left: 0;
        position: fixed;
        width: 100%;
        height: 100%;
        /* display: none; */
        align-items: center;
        justify-content: center;
        background-color: rgba(0, 0, 0, 0.8);
    }

    #Cartmenu {
        background-color: #fff;
        padding: 5vw;
    }

    #closeCart {
        text-decoration: none;
        position: fixed;
        bottom: 0;
        right: 5px;
        border-radius: 25px;
        border: solid black 3px;
        background-color: red;
    }
</style>