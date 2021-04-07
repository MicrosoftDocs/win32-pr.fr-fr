---
title: Utilisation de l’interface IDirectoryObject
description: Lorsque vous créez un client ADSI en C ou C++ qui utilise la liaison précoce, vous disposez d’une plus grande variété de types de données ADSI utilisables pour votre client s’il appelle l’interface IDirectoryObject au lieu de l’interface IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, utilisation
- ADSI ADSI, à l’aide de, à l’aide de l’interface IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671105"
---
# <a name="using-the-idirectoryobject-interface"></a><span data-ttu-id="f3d81-105">Utilisation de l’interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="f3d81-105">Using the IDirectoryObject Interface</span></span>

<span data-ttu-id="f3d81-106">Lorsque vous créez un client ADSI en C ou C++ qui utilise la liaison précoce, vous disposez d’une plus grande variété de types de données ADSI utilisables pour votre client s’il appelle l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) au lieu de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="f3d81-106">When you create an ADSI client in C or C++ that uses early binding, you will have a wider variety of ADSI data types available to use for your client if it calls the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface instead of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="f3d81-107">L’interface **IDirectoryObject** fournit des méthodes pour prendre en charge un sous-ensemble des propriétés de maintenance d’un objet et pour accéder à ses attributs.</span><span class="sxs-lookup"><span data-stu-id="f3d81-107">The **IDirectoryObject** interface provides methods to support a subset of an object's maintenance properties and to access its attributes.</span></span> <span data-ttu-id="f3d81-108">L’illustration suivante montre les relations entre les structures de données.</span><span class="sxs-lookup"><span data-stu-id="f3d81-108">The following figure shows the relationships among the data structures.</span></span>

![structures de données de l’interface idirectoryobject](images/ds2dso.png)

<span data-ttu-id="f3d81-110">Dans la figure précédente, les [**\_ \_ informations sur l’objet structure ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info) définissent les propriétés qui identifient l’objet par nom unique, nom unique relatif, par conteneur (ParentDN), par type d’objet (ClassDN) et par définition de schéma (SchemaDN).</span><span class="sxs-lookup"><span data-stu-id="f3d81-110">In the preceding figure, the structure [**ADS\_OBJECT\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) defines properties that identify the object by distinguished name, relative distinguished name, by container (ParentDN), by object type (ClassDN), and by schema definition (SchemaDN).</span></span> <span data-ttu-id="f3d81-111">Le descripteur d’attribut [**ADS \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) se compose d’un nom, d’un type de données, d’un tableau de valeurs de données affichées dans [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)et d’un indicateur qui indique au service d’annuaire sous-jacent d’effectuer certaines opérations sur les attributs détaillés dans les [ \_ \_ \* constantes de publicités attr](adsi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f3d81-111">The attribute descriptor [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consists of a name, data type, an array of data values shown in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue), and a flag that directs the underlying directory service to perform certain operations on the attributes detailed in [ADS\_ATTR\_\* constants](adsi-constants.md).</span></span> <span data-ttu-id="f3d81-112">Les types de données de ces attributs incluent les types syntaxiques étendus ADSI, détaillés dans [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span><span class="sxs-lookup"><span data-stu-id="f3d81-112">The data types for these attributes include the ADSI extended syntax types, detailed in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span></span>

 

 




