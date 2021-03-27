---
description: Les valeurs d’indicateur SFGAO des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Utilisation des attributs d’élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864913"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="27b6c-103">Utilisation des attributs d’élément</span><span class="sxs-lookup"><span data-stu-id="27b6c-103">How to Use Item Attributes</span></span>

<span data-ttu-id="27b6c-104">Les valeurs d’indicateur [**SFGAO**](sfgao.md) des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="27b6c-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="27b6c-105">Pour utiliser cette fonctionnalité d’attribut, ajoutez les valeurs **reg \_ DWORD** suivantes sous le verbe :</span><span class="sxs-lookup"><span data-stu-id="27b6c-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="27b6c-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="27b6c-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="27b6c-107">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="27b6c-107">Step 1:</span></span>

<span data-ttu-id="27b6c-108">La valeur AttributeMask spécifie la valeur [**SFGAO**](sfgao.md) des valeurs de bit du masque avec lequel effectuer le test.</span><span class="sxs-lookup"><span data-stu-id="27b6c-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="27b6c-109">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="27b6c-109">Step 2:</span></span>

<span data-ttu-id="27b6c-110">La valeur AttributeValue spécifie la valeur [**SFGAO**](sfgao.md) des bits qui sont testés.</span><span class="sxs-lookup"><span data-stu-id="27b6c-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="27b6c-111">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="27b6c-111">Step 3:</span></span>

<span data-ttu-id="27b6c-112">Le ImpliedSelectionModel spécifie zéro pour les verbes d’élément, ou une valeur différente de zéro pour les verbes dans le menu contextuel d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="27b6c-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b6c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="27b6c-113">Remarks</span></span>

<span data-ttu-id="27b6c-114">Dans l’exemple d’entrée de Registre suivant, AttributeMask est défini sur [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="27b6c-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



