---
description: La base de données du produit contient des informations sur un produit. Pour plus d’informations sur l’obtention d’informations sur les produits avec des fonctions d’énumération, consultez initialisation d’une application.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtention d’informations sur l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951517"
---
# <a name="getting-application-information"></a><span data-ttu-id="7e9c0-104">Obtention d’informations sur l’application</span><span class="sxs-lookup"><span data-stu-id="7e9c0-104">Getting Application Information</span></span>

<span data-ttu-id="7e9c0-105">La base de données du produit contient des informations sur un produit.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-105">The product database contains information about a product.</span></span> <span data-ttu-id="7e9c0-106">Pour plus d’informations sur l’obtention d’informations sur les produits avec des fonctions d’énumération, consultez [initialisation d’une application](initializing-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="7e9c0-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="7e9c0-107">**Pour recevoir des informations sur le produit**</span><span class="sxs-lookup"><span data-stu-id="7e9c0-107">**To get product information**</span></span>

1.  <span data-ttu-id="7e9c0-108">Vérifiez qu’un produit est installé en appelant la fonction [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .</span><span class="sxs-lookup"><span data-stu-id="7e9c0-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="7e9c0-109">Ouvrez la base de données et obtenez un handle pour celle-ci en appelant la fonction [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .</span><span class="sxs-lookup"><span data-stu-id="7e9c0-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="7e9c0-110">Si la base de données est contenue dans un package d’installation, appelez la fonction [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .</span><span class="sxs-lookup"><span data-stu-id="7e9c0-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="7e9c0-111">Utilisez le descripteur Open pour obtenir les propriétés du produit avec la fonction [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) et pour obtenir des informations descriptives sur les fonctionnalités avec la fonction [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .</span><span class="sxs-lookup"><span data-stu-id="7e9c0-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="7e9c0-112">Si vous souhaitez obtenir des informations sur le produit à l’aide du code du produit, au lieu d’utiliser le handle de base de données ouvert, appelez la fonction [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) à la place de [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span><span class="sxs-lookup"><span data-stu-id="7e9c0-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="7e9c0-113">Fermez un handle d’installation ouvert en appelant la fonction [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="7e9c0-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="7e9c0-114">La fonction [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) est une fonction de diagnostic et ne doit pas être utilisée pour fermer les descripteurs que vous savez être ouverts.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="7e9c0-115">Il est acceptable d’appeler la fonction **MsiCloseAllHandles** lorsque l’application se ferme pour s’assurer que tous les handles ont été fermés.</span><span class="sxs-lookup"><span data-stu-id="7e9c0-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



