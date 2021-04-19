---
description: Propriétés d’extension MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propriétés d’extension MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537039"
---
# <a name="mtp-extension-properties"></a><span data-ttu-id="3a654-103">Propriétés d’extension MTP</span><span class="sxs-lookup"><span data-stu-id="3a654-103">MTP Extension Properties</span></span>

<span data-ttu-id="3a654-104">Les propriétés décrivent les objets, les propriétés, les ressources et les périphériques.</span><span class="sxs-lookup"><span data-stu-id="3a654-104">Properties describe objects, properties, resources, and devices.</span></span>

## <a name="vendor-extended-object-properties"></a><span data-ttu-id="3a654-105">Fournisseur-propriétés de l’objet étendu</span><span class="sxs-lookup"><span data-stu-id="3a654-105">Vendor-Extended Object Properties</span></span>

<span data-ttu-id="3a654-106">Quand un fabricant de périphériques crée une propriété étendue par un fournisseur pour un objet périphérique, il combine les **Propriétés wpd GUID du \_ fournisseur MTP de l' \_ \_ \_ \_ objet étendu \_** avec le code de propriété de l’objet pour construire une structure **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="3a654-106">When a device manufacturer creates a vendor-extended property for a device object, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_OBJECT\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="3a654-107">Par exemple, si le code de propriété de l’objet est 0xD801, la **PROPERTYKEY** résultante serait comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3a654-107">For example, if the object's property code is 0xD801, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a><span data-ttu-id="3a654-108">Fournisseur-propriétés de l’appareil étendues</span><span class="sxs-lookup"><span data-stu-id="3a654-108">Vendor-Extended Device Properties</span></span>

<span data-ttu-id="3a654-109">Quand un fabricant de périphériques crée une propriété étendue par un fournisseur pour un appareil, il combine les **Propriétés wpd GUID des \_ propriétés d' \_ \_ \_ \_ appareils \_ étendus du fournisseur MTP** avec le code de propriété de l’objet pour construire une structure **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="3a654-109">When a device manufacturer creates a vendor-extended property for a device, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_DEVICE\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="3a654-110">Par exemple, si le code de propriété de l’objet est 0xD001, la **PROPERTYKEY** résultante serait comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3a654-110">For example, if the object's property code is 0xD001, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a><span data-ttu-id="3a654-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a654-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a654-112">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="3a654-112">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



