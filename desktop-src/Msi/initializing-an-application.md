---
description: Pour activer la fonctionnalité du programme d’installation, une application doit appeler un certain nombre de fonctions lors de son initialisation.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Initialisation d’une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202535"
---
# <a name="initializing-an-application"></a>Initialisation d’une application

Pour activer la fonctionnalité du programme d’installation, une application doit appeler un certain nombre de fonctions lors de son initialisation. Pour plus d’informations, consultez [mécanisme d’installation](installation-mechanism.md). Les étapes suivantes décrivent comment utiliser le programme d’installation pour initialiser une application :

**Pour initialiser une application**

1.  Appelez la fonction [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) pour que l’application puisse s’identifier dans le programme d’installation.

    Le code du produit est un paramètre obligatoire pour de nombreuses fonctions du programme d’installation.

2.  Appelez la fonction [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) pour collecter les informations utilisateur lors du premier démarrage de l’application.

    Si l’appel à [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) échoue, appelez la fonction [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) pour collecter des informations sur l’utilisateur.

3.  Affichez une interface utilisateur par défaut, si nécessaire, en appelant la fonction [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

    Pour créer votre propre interface utilisateur, inscrivez-la auprès du programme d’installation en appelant la fonction [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .

4.  Appelez la fonction [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) pour définir le niveau de journalisation.
5.  Présentez à l’utilisateur les fonctionnalités disponibles en énumérant les fonctionnalités de votre application. Vous pouvez énumérer les fonctionnalités des manières suivantes :
    -   Interrogez la fonctionnalité d’installation par fonctionnalité. Par exemple, avant que l’application ne dessine un bouton ou un élément de menu, l’application appelle la fonction [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) afin que le programme d’installation puisse vérifier que la fonctionnalité est disponible.
    -   Énumérer toutes les fonctionnalités disponibles à la fois en appelant la fonction [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) . Pour utiliser cette fonction, l’application doit appeler **MsiEnumFeatures** à plusieurs reprises lors de l’incrémentation d’un index.
6.  Obtenir des informations détaillées sur l’installation actuelle en appelant plusieurs fois les fonctions d’énumération suivantes, en incrémentant une variable d’index pour chaque appel :

    -   Appelez la fonction [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) pour énumérer les produits enregistrés avec le programme d’installation.
    -   Appelez la fonction [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) pour énumérer les composants.
    -   Appelez la fonction [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) pour énumérer les qualificateurs de composants.
    -   Appelez la fonction [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) pour énumérer les produits pour un composant particulier.

    Si la valeur de retour d’une fonction d’énumération est une erreur de \_ réussite, il y a encore plus d’éléments à énumérer et la fonction doit être appelée à nouveau avec une variable d’index incrémentée. Si la valeur de retour est \_ \_ une erreur plus aucun \_ élément, tous les éléments ont été énumérés et la fonction ne doit pas être rappelée.

 

 



