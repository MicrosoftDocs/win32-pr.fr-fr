---
title: UI_PKEY_Label
description: Identifie la propriété de l’étiquette de l’interface utilisateur \_ \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840301"
---
# <a name="ui_pkey_label"></a><span data-ttu-id="45be4-103">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="45be4-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="45be4-104">Identifie la propriété de l’étiquette de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="45be4-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="45be4-105">Notes</span><span class="sxs-lookup"><span data-stu-id="45be4-105">Remarks</span></span>

<span data-ttu-id="45be4-106">L' \_ \_ étiquette de groupe de caractères de l’interface utilisateur est utilisée par une application pour interroger le texte d’étiquette des onglets, des groupes, des boutons, des éléments de la Galerie et d’autres contrôles du ruban.</span><span class="sxs-lookup"><span data-stu-id="45be4-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="45be4-107">Windows 8 et versions ultérieures : l’image du bouton de menu de l' [application](windowsribbon-controls-applicationmenu.md) a été changée en étiquette : **fichier**.</span><span class="sxs-lookup"><span data-stu-id="45be4-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="45be4-108">Nous vous recommandons de ne pas utiliser de fichier comme étiquette pour vos propres onglets.</span><span class="sxs-lookup"><span data-stu-id="45be4-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="45be4-109">La valeur de la propriété est une chaîne limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="45be4-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="45be4-110">Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="45be4-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="45be4-111">L’alignement à droite n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="45be4-111">Right alignment is not supported.</span></span>

<span data-ttu-id="45be4-112">La longueur maximale de l’étiquette de nom de la base de l’interface utilisateur \_ \_ est illimitée.</span><span class="sxs-lookup"><span data-stu-id="45be4-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="45be4-113">Si une commande est exposée à l’aide d’un élément de menu et que la valeur de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou de l’étiquette de l’interface utilisateur \_ \_ contient une lettre précédée d’une esperluette, comme indiqué dans l’exemple suivant, cette lettre est traitée comme une touche d’accès et une touche d’accès rapide pour cette commande par l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="45be4-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="45be4-114">Pour afficher une esperluette dans une étiquette, échappez la désignation de caractères spéciaux par une double esperluette ( `&&` ), comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="45be4-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="45be4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45be4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45be4-116">Propriétés de la ressource</span><span class="sxs-lookup"><span data-stu-id="45be4-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="45be4-117">**Commande. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="45be4-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="45be4-118">IU \_ \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="45be4-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




