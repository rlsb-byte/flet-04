# flet-04
Atividade avaliativa flet número 4
import flet as ft

def main(page: ft.Page):
    page.title = "Flet"
    page.vertical_alignment = ft.MainAxisAlignment.CENTER
    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER

    titulo = ft.Text(
        "Antonio Sincurá",
        size=30,
        weight=ft.FontWeight.BOLD
    )

    subtitulo = ft.Text(
        "Técnico em Informática - Turma 2º Ano (IFNMG)\n"
        "Estou gostando muito de aprender Python!",
        size=16,
        text_align=ft.TextAlign.CENTER
    )

    banner = ft.Image(
        src="https://picsum.photos/300/200",
        width=300,
        height=200,
        fit=ft.BoxFit.COVER,
        border_radius=ft.BorderRadius.all(10)
    )

    botoes = ft.Row(
        controls=[
            ft.Button(content="Meu Perfil"),
            ft.Button(content="Projetos"),
            ft.OutlinedButton(content="Contato"),
        ],
        alignment=ft.MainAxisAlignment.CENTER
    )

    coluna_principal = ft.Column(
        controls=[
            titulo,
            subtitulo,
            banner,
            botoes,
        ],
        horizontal_alignment=ft.CrossAxisAlignment.CENTER,
        alignment=ft.MainAxisAlignment.CENTER,
        spacing=20
    )

    page.add(coluna_principal)

ft.run(main)

