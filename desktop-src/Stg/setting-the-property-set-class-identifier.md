---
title: Définition de l’identificateur de classe du jeu de propriétés
description: La méthode IPropertyStorage SetClass définit à la fois le CLSID de l’objet de stockage et la valeur de balise de classe stockée dans le jeu de propriétés COM. Cela se produit lorsqu’il est appelé sur un stockage de propriété non simple stocké dans un objet de stockage structuré.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Définition de l’identificateur de classe du jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029651"
---
# <a name="setting-the-property-set-class-identifier"></a><span data-ttu-id="1cdc6-105">Définition de l’identificateur de classe du jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="1cdc6-105">Setting the Property Set Class Identifier</span></span>

<span data-ttu-id="1cdc6-106">La méthode [**IPropertyStorage :: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) définit à la fois le CLSID de l’objet de stockage et la valeur de balise de classe stockée dans le jeu de propriétés com.</span><span class="sxs-lookup"><span data-stu-id="1cdc6-106">The [**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) method sets both the CLSID of the storage object and the class tag value stored in the COM property set.</span></span> <span data-ttu-id="1cdc6-107">Cela se produit lorsqu’il est appelé sur un stockage de propriété non simple stocké dans un objet de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="1cdc6-107">This occurs when invoked on a nonsimple property storage stored in a structured storage object.</span></span>

<span data-ttu-id="1cdc6-108">Cela fournit une cohérence et une uniformité qui crée une meilleure interaction avec certains outils.</span><span class="sxs-lookup"><span data-stu-id="1cdc6-108">This provides consistency and uniformity which creates better interaction with some tools.</span></span> <span data-ttu-id="1cdc6-109">Un objet de stockage de propriétés n’est pas simple s’il est créé en appelant [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) avec l’indicateur **PROPSETFLAG non \_ simple** défini.</span><span class="sxs-lookup"><span data-stu-id="1cdc6-109">A property storage object is nonsimple if it is created by calling [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) with the **PROPSETFLAG\_NONSIMPLE** flag set.</span></span>

<span data-ttu-id="1cdc6-110">Le CLSID de l’objet de stockage est défini avec un appel à [**IStorage :: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span><span class="sxs-lookup"><span data-stu-id="1cdc6-110">The CLSID of the storage object is set with a call to [**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span></span>

 

 




