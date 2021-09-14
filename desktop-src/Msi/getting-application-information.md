---
description: La base de données du produit contient des informations sur un produit. Pour plus d’informations sur l’obtention d’informations sur les produits avec des fonctions d’énumération, consultez initialisation d’une application.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtention d’informations sur l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021676"
---
# <a name="getting-application-information"></a>Obtention d’informations sur l’application

La base de données du produit contient des informations sur un produit. Pour plus d’informations sur l’obtention d’informations sur les produits avec des fonctions d’énumération, consultez [initialisation d’une application](initializing-an-application.md).

**Pour recevoir des informations sur le produit**

1.  Vérifiez qu’un produit est installé en appelant la fonction [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .
2.  Ouvrez la base de données et obtenez un handle pour celle-ci en appelant la fonction [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .

    Si la base de données est contenue dans un package d’installation, appelez la fonction [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .

3.  Utilisez le descripteur Open pour obtenir les propriétés du produit avec la fonction [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) et pour obtenir des informations descriptives sur les fonctionnalités avec la fonction [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .

    Si vous souhaitez obtenir des informations sur le produit à l’aide du code du produit, au lieu d’utiliser le handle de base de données ouvert, appelez la fonction [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) à la place de [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).

4.  Fermez un handle d’installation ouvert en appelant la fonction [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .

    La fonction [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) est une fonction de diagnostic et ne doit pas être utilisée pour fermer les descripteurs que vous savez être ouverts. Il est acceptable d’appeler la fonction **MsiCloseAllHandles** lorsque l’application se ferme pour s’assurer que tous les handles ont été fermés.

 

 



