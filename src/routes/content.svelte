<script>
    let domain_name;
    let domain;
    let price = 0;

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

        <p>IDR. {price} <button>Add to chart</button> </p>
        </center>
</div>