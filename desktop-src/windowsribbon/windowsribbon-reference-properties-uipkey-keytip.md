---
title: UI_PKEY_Keytip
description: Identifie la propriété de KeyTip de l’interface utilisateur \_ \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940031"
---
# <a name="ui_pkey_keytip"></a><span data-ttu-id="1b03d-103">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="1b03d-103">UI\_PKEY\_Keytip</span></span>

<span data-ttu-id="1b03d-104">Identifie la propriété de KeyTip de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b03d-104">Identifies the UI\_PKEY\_Keytip property.</span></span>

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="1b03d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1b03d-105">Remarks</span></span>

<span data-ttu-id="1b03d-106">L’interface utilisateur de \_ \_ la touche d’accès rapide est utilisée par une application pour interroger l’accélérateur clavier d’un contrôle de ruban.</span><span class="sxs-lookup"><span data-stu-id="1b03d-106">UI\_PKEY\_Keytip is used by an application to query the keyboard accelerator of a ribbon control.</span></span>

<span data-ttu-id="1b03d-107">Cette valeur de propriété est une chaîne, composée d’une séquence de caractères, y compris un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="1b03d-107">This property value is a string, composed of any sequence of characters including white space.</span></span>

<span data-ttu-id="1b03d-108">La valeur de l’interface utilisateur de la touche d’accès \_ \_ rapide agit comme touche d’accès rapide pour une commande, sauf si cette commande est exposée par le biais d’un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="1b03d-108">The value of UI\_PKEY\_Keytip acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="1b03d-109">Dans ce cas, le Framework ignore la valeur de KeyTip KeyTip de l’interface utilisateur \_ \_ et utilise à la place un caractère précédé d’un signe & comme spécifié par la [**commande. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [l’étiquette du \_ \_ nom de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="1b03d-109">In this case, the framework ignores the UI\_PKEY\_Keytip value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="1b03d-110">Si aucune esperluette n’est spécifiée par la **commande. LabelTitle** ou l' \_ \_ étiquette de nom de l’interface utilisateur, aucune touche d’accès ou touche d’accès rapide n’est exposée.</span><span class="sxs-lookup"><span data-stu-id="1b03d-110">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="1b03d-111">La longueur maximale de la touche d’entrée de l’interface utilisateur \_ \_ est illimitée.</span><span class="sxs-lookup"><span data-stu-id="1b03d-111">The maximum length of UI\_PKEY\_Keytip is unbounded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b03d-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b03d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b03d-113">Propriétés de la ressource</span><span class="sxs-lookup"><span data-stu-id="1b03d-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="1b03d-114">**Commande. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="1b03d-114">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




