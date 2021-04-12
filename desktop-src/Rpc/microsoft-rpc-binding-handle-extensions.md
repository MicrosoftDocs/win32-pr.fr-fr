---
title: Extensions de Binding-Handle Microsoft RPC
description: Les extensions Microsoft du langage IDL prennent en charge plusieurs paramètres de handle qui apparaissent dans des positions autres que le premier paramètre, le plus à gauche.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104032003"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Extensions de Binding-Handle Microsoft RPC

Les extensions Microsoft du langage IDL prennent en charge plusieurs paramètres de handle qui apparaissent dans des positions autres que le premier paramètre, le plus à gauche. Les étapes suivantes décrivent la séquence que le compilateur MIDL passe pour résoudre le paramètre de handle de liaison en mode de compatibilité DCE (/**OSF**) et en mode par défaut (étendu Microsoft).

## <a name="dce-compatibility-mode"></a>DCE-mode de compatibilité

-   Handle de liaison qui apparaît à la première position.
-   \[ [**À l'**](/windows/desktop/Midl/in)extrême gauche, paramètre de [**\_ handle de contexte**](/windows/desktop/Midl/context-handle) \] .
-   Handle de liaison implicite spécifié par un handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) \] ou un \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .
-   Si aucun CCP n’est présent, utilise par défaut le \[ **\_ descripteur automatique** \] .

## <a name="default-mode"></a>Mode par défaut

-   Handle de liaison explicite le plus à gauche.
-   Handle de liaison implicite spécifié par un handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) \] ou un \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .
-   Si aucun CCP n’est présent, utilise par défaut le \[ [**\_ descripteur automatique**](/windows/desktop/Midl/auto-handle) \] .

Les compilateurs IDL DCE recherchent un handle de liaison explicite comme premier paramètre. Lorsque le premier paramètre n’est pas un handle de liaison et qu’un ou plusieurs descripteurs de contexte sont spécifiés, le descripteur de contexte le plus à gauche est utilisé comme handle de liaison. Lorsque le premier paramètre n’est pas un handle et qu’il n’existe aucun descripteur de contexte, la procédure utilise une liaison implicite à l’aide du handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) de l’attribut ACF \] ou du \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .

Les extensions Microsoft de l’IDL permettent au handle de liaison d’être dans une position autre que le premier paramètre. Le plus \[ [**à gauche dans**](/windows/desktop/Midl/in) le \] paramètre de handle explicite, qu’il s’agisse d’un handle primitif, défini par le programmeur ou d’un handle de contexte, est le handle de liaison. Lorsqu’il n’y a aucun paramètre de handle, la procédure utilise une liaison implicite à l’aide du handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) de l’attribut ACF \] ou du \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .

Les règles suivantes s’appliquent à la fois au mode de compatibilité DCE (/OSF) et au mode par défaut :

-   La liaison de gestion automatique est utilisée quand aucun CCP n’est présent.
-   \[ [](/windows/desktop/Midl/in) \] Descripteurs in ou \[ **in**, [**out**](/windows/desktop/Midl/out-idl) explicites \] pour une fonction individuelle preempt toute liaison implicite spécifiée pour l’interface.
-   Plusieurs \[ [](/windows/desktop/Midl/in) \] \[ Handles de primitives in ou **in**, out \] ne sont pas pris en charge.
-   Plusieurs \[ [](/windows/desktop/Midl/in) \] \[ Handles de contexte explicites in ou **in**, out \] sont autorisés.
-   Tous les paramètres de handle définis par le programmeur, à l’exception du paramètre de handle de liaison, sont traités comme des données transmissibles.

Le tableau suivant contient des exemples et décrit comment les handles de liaison sont assignés dans chaque mode de compilateur.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Exemple</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td>Aucun handle explicite n’est spécifié. Le handle de liaison implicite, spécifié par [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] ou [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], est utilisé. Quand aucun CCP n’est présent, un descripteur automatique est utilisé.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td>Un handle explicite de type handle_t est spécifié. Le paramètre <em>H</em> est le handle de liaison de la procédure.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td>Le premier paramètre n’est pas un descripteur. En mode par défaut, le paramètre de handle le plus à gauche, <em>H</em>, est le handle de liaison. En mode/OSF, la liaison implicite est utilisée. Une erreur est signalée, car le deuxième paramètre est supposé être transmissible et handle_t ne peut pas être transmis.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td>Le premier paramètre n’est pas un descripteur. En mode par défaut, le paramètre de handle le plus à gauche, <em>H</em>, est le handle de liaison. Les stubs appellent les routines fournies par l’utilisateur MY_HDL_bind et MY_HDL_unbind. En mode OSF, la liaison implicite est utilisée. Le paramètre de descripteur défini par le programmeur <em>H</em> est traité comme des données transmissibles.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td>Le premier paramètre est un handle de liaison. Le paramètre <em>H</em> est le paramètre de handle de liaison. Le deuxième paramètre de handle défini par le programmeur est traité comme des données transmissibles.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td>Le handle de liaison est un handle de contexte. Le paramètre <em>H</em> est le handle de liaison.</td>
</tr>
</tbody>
</table>



 

 

 