---
description: La propriété DVDAdm fournit l’accès à l’objet MSDVDAdm qui contient des méthodes et des propriétés pour l’enregistrement des informations sur l’application et l’utilisateur.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propriété DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109223"
---
# <a name="dvdadm-property"></a><span data-ttu-id="f7bd0-103">Propriété DVDAdm</span><span class="sxs-lookup"><span data-stu-id="f7bd0-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="f7bd0-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f7bd0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f7bd0-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f7bd0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f7bd0-106">La `DVDAdm` propriété fournit l’accès à l’objet [MSDVDAdm](msdvdadm-object.md) qui contient des méthodes et des propriétés pour l’enregistrement des informations sur l’application et l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7bd0-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="f7bd0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f7bd0-107">Remarks</span></span>

<span data-ttu-id="f7bd0-108">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7bd0-108">This property is read-only with no default value.</span></span> <span data-ttu-id="f7bd0-109">Il n’est pas nécessaire de créer une référence distincte à l’objet **MSDVDAdm** .</span><span class="sxs-lookup"><span data-stu-id="f7bd0-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="f7bd0-110">Pour accéder aux méthodes et aux propriétés de l’objet, utilisez la `DVDAdm` propriété comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f7bd0-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="f7bd0-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="f7bd0-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



