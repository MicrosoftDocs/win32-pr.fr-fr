---
description: 'les utilisateurs et les applications avec des privilèges d’administrateur peuvent utiliser Windows Installer fonctions pour inventorier les applications Windows Installer, les fonctionnalités, les composants et les correctifs installés sur le système. à partir de Windows Installer&\# 160 ; 3.0, les utilisateurs et les applications qui possèdent des privilèges d’administrateur peuvent énumérer les applications, les fonctionnalités, les composants et les correctifs Windows Installer installés sur le système par tous les utilisateurs. Les administrateurs et les applications peuvent obtenir des informations sur un produit ou un correctif pour un utilisateur spécifique ou tous les utilisateurs du système. Les applications peuvent obtenir l’état de la fonctionnalité ou l’état du composant pour un utilisateur particulier. les fonctions d’inventaire disponibles à partir de Windows Installer&\# 160 ; 3.0 peuvent limiter l’étendue des éléments à rechercher dans le contexte de l’installation et le contexte de l’utilisateur. Il existe trois contextes d’installation possibles : par utilisateur, par ordinateur et par utilisateur. Le contexte de l’utilisateur peut être un utilisateur particulier ou tous les utilisateurs du système. les versions de la Windows Installer fonctions d’inventaire antérieures à Windows Installer&\# 160 ; 3.0 peuvent uniquement énumérer les éléments installés sur le système dans le contexte de l’ordinateur ou dans le contexte par utilisateur de l’utilisateur actuel. cette limitation empêche un inventaire complet de tous les produits Windows Installer et des correctifs installés dans le système par des utilisateurs autres que l’utilisateur actuel. Énumération des informations d’État du composant InformationObtaining ProductsEnumerating PatchesObtaining Product InformationObtaining patch InformationObtaining'
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: utilisation de Windows Installer pour inventorier des produits et des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9406d0984e58efdb8344fbf8974234690e3a6aaeb1cc697b5a76e6af940554e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013227"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>utilisation de Windows Installer pour inventorier des produits et des correctifs

les utilisateurs et les applications avec des privilèges d’administrateur peuvent utiliser Windows Installer fonctions pour inventorier les applications Windows Installer, les fonctionnalités, les composants et les correctifs installés sur le système.

à partir de Windows Installer 3,0, les utilisateurs et les applications qui possèdent des privilèges d’administrateur peuvent énumérer les Windows Installer applications, fonctionnalités, composants et correctifs installés sur le système par tous les utilisateurs. Les administrateurs et les applications peuvent obtenir des informations sur un produit ou un correctif pour un utilisateur spécifique ou tous les utilisateurs du système. Les applications peuvent obtenir l’état de la fonctionnalité ou l’état du composant pour un utilisateur particulier.

les fonctions d’inventaire disponibles à partir de Windows Installer 3,0 peuvent limiter l’étendue des éléments à rechercher dans le contexte de l’installation et dans le contexte de l’utilisateur. Il existe trois contextes d’installation possibles : par utilisateur, par ordinateur et par utilisateur. Le contexte de l’utilisateur peut être un utilisateur particulier ou tous les utilisateurs du système.

les versions des fonctions d’inventaire Windows Installer antérieures à Windows Installer 3,0 peuvent uniquement énumérer les éléments installés sur le système dans le contexte de l’ordinateur ou dans le contexte par utilisateur de l’utilisateur actuel. cette limitation empêche un inventaire complet de tous les produits Windows Installer et des correctifs installés dans le système par des utilisateurs autres que l’utilisateur actuel.

-   [Énumération des produits](#enumerating-products)
-   [Énumération des correctifs](#enumerating-patches)
-   [Obtention d’informations sur le produit](#obtaining-product-information)
-   [Obtention d’informations sur les correctifs](#obtaining-patch-information)
-   [Obtention d’informations sur l’état du composant](#obtaining-component-state-information)
-   [Obtention d’informations sur l’état des fonctionnalités](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Énumération des produits

utilisez la fonction [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) pour énumérer Windows Installer les applications qui sont installées dans le système. Cette fonction peut trouver toutes les installations par ordinateur et les installations par utilisateur des applications (gérées et non gérées) pour l’utilisateur actuel et les autres utilisateurs du système. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation à trouver. Vous pouvez spécifier n’importe quelle combinaison des contextes d’installation possibles. Utilisez le paramètre *szUserSid* pour spécifier le contexte utilisateur des applications à trouver.

## <a name="enumerating-patches"></a>Énumération des correctifs

Utilisez la fonction [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) pour rechercher les correctifs appliqués à une application. Cette fonction peut rechercher les correctifs appliqués à une application particulière ou à toutes les applications du système. Cette fonction peut trouver les correctifs appliqués à toutes les installations par ordinateur et aux installations par utilisateur des applications (gérées et non gérées) pour l’utilisateur actuel et les autres utilisateurs du système.

Vous pouvez utiliser le contexte d’installation et le contexte utilisateur pour limiter l’énumération des correctifs à un contexte particulier ou dans tous les contextes. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation à trouver. Vous pouvez spécifier n’importe quelle combinaison des contextes d’installation possibles. Utilisez le paramètre *szUserSid* pour spécifier le contexte utilisateur des applications à trouver.

**Pour énumérer les correctifs appliqués à tous les produits publiés ou installés par tous les utilisateurs du système**

-   Appelez la fonction [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) .
    -   Utilisez **null** pour la valeur du paramètre *szProductCode* .
    -   Utilisez « s-1-1-0 » pour la valeur du paramètre *szUserSid* .
    -   Utilisez « MSIINSTALLCONTEXT \_ All » pour la valeur du paramètre *dwContext* .

**Pour énumérer les correctifs appliqués à tous les produits publiés ou installés par tous les utilisateurs du système**

1.  Appelez la fonction [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) .

    -   Utilisez **null** pour la valeur du paramètre *szProductCode* .
    -   Utilisez « s-1-1-0 » pour la valeur du paramètre *szUserSid* .
    -   Utilisez « MSIINSTALLCONTEXT \_ All » pour la valeur du paramètre *dwContext* .

    La fonction fournit un code de produit, un contexte utilisateur et un contexte d’installation pour chaque application trouvée.

2.  Pour chaque application énumérée à l’étape 1, appelez [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) pour énumérer les correctifs.

    Utilisez les codes de produit, les contextes utilisateur et les contextes d’installation obtenus à partir de [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) pour les valeurs de *szProductCode*, *szUserSid* et *dwContext*, ainsi que pour chaque appel de fonction **MsiEnumProductsEx** .

## <a name="obtaining-product-information"></a>Obtention d’informations sur le produit

Utilisez la fonction [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) pour obtenir des informations sur les applications publiées ou installées sur le système, ainsi que sur les propriétés qui peuvent être récupérées. Cette fonction peut obtenir des informations sur une instance d’une application installée sous un compte d’utilisateur autre que l’utilisateur actuel, mais ne peut pas interroger une instance d’un produit publié dans un contexte non géré par utilisateur pour un compte d’utilisateur autre que l’utilisateur actuel.

Vous pouvez spécifier le contexte d’installation et le contexte utilisateur pour restreindre les informations pour les applications installées dans un contexte particulier. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation à trouver. Vous ne pouvez spécifier qu’un seul des contextes d’installation possibles. Utilisez le paramètre *szUserSid* pour spécifier le contexte utilisateur des applications à trouver.

## <a name="obtaining-patch-information"></a>Obtention d’informations sur les correctifs

Une application peut appeler la fonction [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) pour demander des informations sur l’application d’un correctif à une instance spécifiée d’un produit. Les propriétés telles que **LocalPackage**, [**transformations**](transforms.md)et **State** peuvent être récupérées à l’aide de cette fonction. Il n’est pas garanti que toutes les valeurs de propriété soient disponibles pour les applications non gérées par utilisateur si l’utilisateur n’est pas actuellement connecté à l’ordinateur. Vous ne pouvez spécifier qu’un seul des contextes d’installation possibles.

Vous pouvez spécifier le contexte d’installation et le contexte utilisateur pour limiter les informations aux correctifs appliqués aux applications installées dans un contexte particulier. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation à trouver. Vous ne pouvez spécifier qu’un seul des contextes d’installation possibles. Utilisez le paramètre *szUserSid* pour spécifier le contexte utilisateur des applications à trouver.

## <a name="obtaining-component-state-information"></a>Obtention d’informations sur l’état du composant

Les applications peuvent appeler la fonction [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) pour obtenir l’état d’installation d’un composant. Cette fonction détermine si le composant est installé localement ou s’il est installé pour être exécuté à partir de la source. La fonction peut rechercher un composant d’une instance d’une application qui est installée sous des comptes d’utilisateurs autres que l’utilisateur actuel, à condition que le produit ne soit pas publié sous le contexte non géré par utilisateur pour un compte d’utilisateur autre que l’utilisateur actuel.

Vous pouvez spécifier un contexte d’installation et un contexte utilisateur pour obtenir l’état des composants pour les applications installées dans un contexte particulier. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation à trouver. Vous ne pouvez spécifier qu’un seul des contextes d’installation possibles. Utilisez le paramètre *szUserSid* pour spécifier le contexte utilisateur des applications à trouver.

## <a name="obtaining-feature-state-information"></a>Obtention d’informations sur l’état des fonctionnalités

Les applications peuvent appeler la fonction [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) pour obtenir l’état d’installation d’une fonctionnalité de produit. Cette fonction détermine si la fonctionnalité est publiée, installée localement ou installée pour être exécutée à partir de la source. La fonction peut être utilisée pour interroger n’importe quelle fonctionnalité d’une instance d’une application installée sous le compte de l’ordinateur ou n’importe quel contexte sous le compte d’utilisateur actuel ou le contexte géré par utilisateur sous n’importe quel compte d’utilisateur autre que l’utilisateur actuel. Cette fonction ne peut pas rechercher une application installée dans le contexte non géré par utilisateur pour un compte d’utilisateur autre que l’utilisateur actuel. Vous ne pouvez spécifier qu’un seul des contextes d’installation possibles.

Vous pouvez spécifier un contexte d’installation et un contexte utilisateur pour obtenir l’état des fonctionnalités pour les applications installées dans un contexte particulier. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation à trouver. Vous ne pouvez spécifier qu’un seul des contextes d’installation possibles. Utilisez le paramètre *szUserSid* pour spécifier le contexte utilisateur des applications à trouver.

 

 



