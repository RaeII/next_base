# Lista de Componentes

Este documento lista os componentes disponíveis no projeto e suas funcionalidades.
Os componentes estão localizados principalmente em `src/components`.

## UI Components (`src/components/ui`)

Estes são componentes de interface reutilizáveis, geralmente primitivos de UI.

### Input (`src/components/ui/input.tsx`)
**Descrição:** Componente de entrada de texto estilizável.
**Utilidade:** Utilizado para criar campos de formulário, barras de pesquisa e qualquer outra entrada de dados textual. Baseado no elemento HTML `<input>` nativo, aceitando todas as suas propriedades padrão, mas estilizado com classes utilitárias do Tailwind.
**Props principais:** Aceita todas as props padrão de `React.ComponentProps<"input">`.

### Toaster (`src/components/ui/sonner.tsx`)
**Descrição:** Componente de notificação (toast) para feedback ao usuário.
**Utilidade:** Gerencia e exibe notificações temporárias (sucesso, erro, info, etc.) no canto da tela. Utiliza a biblioteca `sonner` por baixo dos panos. Deve ser adicionado na raiz do layout (geralmente em `src/app/layout.tsx`) para funcionar globalmente.
**Características:**
- Integração com `next-themes` para suporte a temas (claro/escuro/sistema).
- Ícones personalizados para diferentes tipos de mensagens (sucesso, erro, info, aviso).

### Button (`src/components/ui/button.tsx`)
**Descrição:** Botão padrão interativo.
**Utilidade:** Utilizado para ações principais e secundárias. Suporta variantes chamadas `default`, `destructive`, `outline`, `secondary`, `ghost`, e `link`.

### Card (`src/components/ui/card.tsx`)
**Descrição:** Container flexível e extensível.
**Utilidade:** Agrupa componentes relacionados. Composto por `Card`, `CardHeader`, `CardTitle`, `CardDescription`, `CardContent`, e `CardFooter`.

### Label (`src/components/ui/label.tsx`)
**Descrição:** Rótulo acessível para elementos de formulário.
**Utilidade:** Usado em conjunto com inputs para garantir acessibilidade e clareza. Baseado no Radix UI Label.

### Form (`src/components/ui/form.tsx`)
**Descrição:** Wrapper para formulários com `react-hook-form` e `zod`.
**Utilidade:** Simplifica a criação de formulários tipados e com validação, integrando mensagens de erro e acessibilidade automaticamente.

## Feature Components

### LoginForm (`src/app/(auth)/login/components/login-form.tsx`)
**Descrição:** Formulário de login com validação.
**Utilidade:** Permite ao usuário autenticar-se. Utiliza `react-hook-form` com validação `zod` e componentes UI (Card, Input, Button, Form). Localizado junto à página de login.

### ThemeProvider (`src/components/theme-provider.tsx`)
**Descrição:** Provedor de contexto para gerenciar temas (claro/escuro).
**Utilidade:** Envolve a aplicação para permitir a troca de temas via `next-themes`.

### ModeToggle (`src/components/mode-toggle.tsx`)
**Descrição:** Botão para alternar entre temas claro, escuro e sistema.
**Utilidade:** Interface de usuário para controle do tema, utilizando um menu dropdown acessível. Posicionado globalmente no layout.
