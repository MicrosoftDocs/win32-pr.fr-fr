---
title: Ressource ACCÉLÉRATEURs
description: Définit un ou plusieurs accélérateurs pour une application. Un accélérateur est une séquence de touches définie par l’application pour offrir à l’utilisateur un moyen rapide d’effectuer une tâche.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menus des ressources des ACCÉLÉRATEURs et autres ressources
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507890"
---
# <a name="accelerators-resource"></a><span data-ttu-id="3c5fe-105">Ressource ACCÉLÉRATEURs</span><span class="sxs-lookup"><span data-stu-id="3c5fe-105">ACCELERATORS resource</span></span>

<span data-ttu-id="3c5fe-106">Définit un ou plusieurs accélérateurs pour une application.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="3c5fe-107">Un accélérateur est une séquence de touches définie par l’application pour offrir à l’utilisateur un moyen rapide d’effectuer une tâche.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="3c5fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c5fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5fe-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="3c5fe-110">Nom unique ou valeur d’entier non signé 16 bits qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3c5fe-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="3c5fe-112">Zéro, une ou plusieurs des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="3c5fe-113">.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-113">Statement</span></span>                                                        | <span data-ttu-id="3c5fe-114">Description</span><span class="sxs-lookup"><span data-stu-id="3c5fe-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5fe-115">[**Caractéristiques**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="3c5fe-116">Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="3c5fe-117">Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="3c5fe-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="3c5fe-118">[](language-statement.md) *Langue* langue, sous- *langue*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="3c5fe-119">Spécifie la langue de la ressource.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-119">Specifies the language for the resource.</span></span> <span data-ttu-id="3c5fe-120">Pour plus d’informations, consultez [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="3c5fe-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="3c5fe-121">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="3c5fe-122">Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="3c5fe-123">Pour plus d’informations, consultez [**version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="3c5fe-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="3c5fe-124"><span id="event"></span><span id="EVENT"></span>*événement*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="3c5fe-125">Séquence de touches à utiliser comme accélérateur.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="3c5fe-126">Il peut s’agir de l’un des types de caractères suivants.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="3c5fe-127">Type</span><span class="sxs-lookup"><span data-stu-id="3c5fe-127">Type</span></span>                    | <span data-ttu-id="3c5fe-128">Description</span><span class="sxs-lookup"><span data-stu-id="3c5fe-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5fe-129">«*char*»</span><span class="sxs-lookup"><span data-stu-id="3c5fe-129">"*char*"</span></span>                | <span data-ttu-id="3c5fe-130">Caractère unique placé entre guillemets doubles (").</span><span class="sxs-lookup"><span data-stu-id="3c5fe-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="3c5fe-131">Le caractère peut être précédé d’un signe insertion (^), ce qui signifie que le caractère est un caractère de contrôle.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="3c5fe-132">*Caractère*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-132">*Character*</span></span>             | <span data-ttu-id="3c5fe-133">Valeur entière représentant un caractère.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-133">An integer value representing a character.</span></span> <span data-ttu-id="3c5fe-134">Le paramètre de *type* doit être **ASCII**.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="3c5fe-135">*caractère de clé virtuelle*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-135">*virtual-key character*</span></span> | <span data-ttu-id="3c5fe-136">Valeur entière représentant une clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="3c5fe-137">La clé virtuelle pour les clés alphanumériques peut être spécifiée en plaçant la lettre majuscule ou le nombre entre guillemets doubles (par exemple, « 9 » ou « C »).</span><span class="sxs-lookup"><span data-stu-id="3c5fe-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="3c5fe-138">Le paramètre de *type* doit être **VIRTKEY**.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3c5fe-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idValue*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="3c5fe-140">valeur entière 16 bits non signée qui identifie l’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="3c5fe-141"><span id="type"></span><span id="TYPE"></span>*entrer*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="3c5fe-142">Obligatoire uniquement lorsque le paramètre d' *événement* est un *caractère* ou un *caractère de clé virtuelle*.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="3c5fe-143">Le paramètre de *type* spécifie **ASCII** ou **VIRTKEY**. la valeur entière de l' *événement* est interprétée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="3c5fe-144">Lorsque **VIRTKEY** est spécifié et que *Event* contient une chaîne, l' *événement* doit être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="3c5fe-145"><span id="options"></span><span id="OPTIONS"></span>*Options*</span><span class="sxs-lookup"><span data-stu-id="3c5fe-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="3c5fe-146">options qui définissent l’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-146">options that define the accelerator.</span></span> <span data-ttu-id="3c5fe-147">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3c5fe-148">Option</span><span class="sxs-lookup"><span data-stu-id="3c5fe-148">Option</span></span>                             | <span data-ttu-id="3c5fe-149">Description</span><span class="sxs-lookup"><span data-stu-id="3c5fe-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5fe-150">**Noinversé**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-150">**NOINVERT**</span></span>                       | <span data-ttu-id="3c5fe-151">Spécifie qu’aucun élément de menu de niveau supérieur n’est mis en surbrillance lorsque l’accélérateur est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="3c5fe-152">Cela est utile lorsque vous définissez des accélérateurs pour des actions telles que le défilement qui ne correspondent pas à un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="3c5fe-153">Si **noinversé** est omis, un élément de menu de niveau supérieur est mis en surbrillance (si possible) quand l’accélérateur est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="3c5fe-154">Cet attribut est obsolète et conservé uniquement à des fins de compatibilité descendante avec les fichiers de ressources conçus pour Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="3c5fe-155">**Alt**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-155">**ALT**</span></span>                            | <span data-ttu-id="3c5fe-156">Entraîne l’activation de l’accélérateur uniquement si la touche ALT est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="3c5fe-157">S’applique uniquement aux clés virtuelles.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3c5fe-158">**MAJUSCULE**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-158">**SHIFT**</span></span>                          | <span data-ttu-id="3c5fe-159">Entraîne l’activation de l’accélérateur uniquement si la touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="3c5fe-160">S’applique uniquement aux clés virtuelles</span><span class="sxs-lookup"><span data-stu-id="3c5fe-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3c5fe-161">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="3c5fe-162">Définit le caractère en tant que caractère de contrôle (l’accélérateur est activé uniquement si la touche de contrôle est enfoncée).</span><span class="sxs-lookup"><span data-stu-id="3c5fe-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="3c5fe-163">Cela a le même effet que l’utilisation d’un signe insertion (^) avant le caractère d’accélérateur dans le paramètre d' *événement* .</span><span class="sxs-lookup"><span data-stu-id="3c5fe-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="3c5fe-164">S’applique uniquement aux clés virtuelles</span><span class="sxs-lookup"><span data-stu-id="3c5fe-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="3c5fe-165">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3c5fe-166">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3c5fe-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c5fe-167">Notes</span><span class="sxs-lookup"><span data-stu-id="3c5fe-167">Remarks</span></span>

<span data-ttu-id="3c5fe-168">La fonction [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) est utilisée pour convertir les messages d’accélérateur de la file d’attente de l’application en messages de [**\_ commande WM**](./wm-command.md) ou [**WM \_ SYSCOMMAND**](./wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="3c5fe-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="3c5fe-169">Exemples</span><span class="sxs-lookup"><span data-stu-id="3c5fe-169">Examples</span></span>

<span data-ttu-id="3c5fe-170">L’exemple suivant illustre l’utilisation de touches accélérateur.</span><span class="sxs-lookup"><span data-stu-id="3c5fe-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="3c5fe-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c5fe-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5fe-172">Utilisation des accélérateurs clavier</span><span class="sxs-lookup"><span data-stu-id="3c5fe-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="3c5fe-174">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-175">**DIALOGUE**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-176">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-177">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-179">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="3c5fe-180">**Version**</span><span class="sxs-lookup"><span data-stu-id="3c5fe-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 