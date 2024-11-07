<template>
    <div>
        <h2>Registro</h2>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre</label>
                <Field name="nombre" id="nombre" type="text" placeholder="ingrese su nombre"/>
                <ErrorMessage name="nombre" ></ErrorMessage>
            </div >
            <div class="form">
                <label for="correo">Correo</label>
                <Field name="email" id="email" type="email" placeholder="ingrese su email"/>
                <ErrorMessage name="email" />
            </div>
            <div class="form">
                <button type="submit">Registrar</button>
            </div>
        </Form>

    </div>
</template>

<script setup>
import { Form, Field, ErrorMessage } from 'vee-validate';
import { schema } from '../schemas/validationSchema';

const onSubmit = () => {
    console.log('congrats your form was submitted');
}
</script>

<style scoped>
.form {
    margin-bottom: 10px;
}
</style>