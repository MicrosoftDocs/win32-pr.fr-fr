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
# <a name="initializing-an-application"></a><span data-ttu-id="598f9-103">Initialisation d’une application</span><span class="sxs-lookup"><span data-stu-id="598f9-103">Initializing an Application</span></span>

<span data-ttu-id="598f9-104">Pour activer la fonctionnalité du programme d’installation, une application doit appeler un certain nombre de fonctions lors de son initialisation.</span><span class="sxs-lookup"><span data-stu-id="598f9-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="598f9-105">Pour plus d’informations, consultez [mécanisme d’installation](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="598f9-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="598f9-106">Les étapes suivantes décrivent comment utiliser le programme d’installation pour initialiser une application :</span><span class="sxs-lookup"><span data-stu-id="598f9-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="598f9-107">**Pour initialiser une application**</span><span class="sxs-lookup"><span data-stu-id="598f9-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="598f9-108">Appelez la fonction [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) pour que l’application puisse s’identifier dans le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="598f9-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="598f9-109">Le code du produit est un paramètre obligatoire pour de nombreuses fonctions du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="598f9-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="598f9-110">Appelez la fonction [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) pour collecter les informations utilisateur lors du premier démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="598f9-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="598f9-111">Si l’appel à [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) échoue, appelez la fonction [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) pour collecter des informations sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="598f9-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="598f9-112">Affichez une interface utilisateur par défaut, si nécessaire, en appelant la fonction [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .</span><span class="sxs-lookup"><span data-stu-id="598f9-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="598f9-113">Pour créer votre propre interface utilisateur, inscrivez-la auprès du programme d’installation en appelant la fonction [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="598f9-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="598f9-114">Appelez la fonction [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) pour définir le niveau de journalisation.</span><span class="sxs-lookup"><span data-stu-id="598f9-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="598f9-115">Présentez à l’utilisateur les fonctionnalités disponibles en énumérant les fonctionnalités de votre application.</span><span class="sxs-lookup"><span data-stu-id="598f9-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="598f9-116">Vous pouvez énumérer les fonctionnalités des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="598f9-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="598f9-117">Interrogez la fonctionnalité d’installation par fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="598f9-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="598f9-118">Par exemple, avant que l’application ne dessine un bouton ou un élément de menu, l’application appelle la fonction [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) afin que le programme d’installation puisse vérifier que la fonctionnalité est disponible.</span><span class="sxs-lookup"><span data-stu-id="598f9-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="598f9-119">Énumérer toutes les fonctionnalités disponibles à la fois en appelant la fonction [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) .</span><span class="sxs-lookup"><span data-stu-id="598f9-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="598f9-120">Pour utiliser cette fonction, l’application doit appeler **MsiEnumFeatures** à plusieurs reprises lors de l’incrémentation d’un index.</span><span class="sxs-lookup"><span data-stu-id="598f9-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="598f9-121">Obtenir des informations détaillées sur l’installation actuelle en appelant plusieurs fois les fonctions d’énumération suivantes, en incrémentant une variable d’index pour chaque appel :</span><span class="sxs-lookup"><span data-stu-id="598f9-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="598f9-122">Appelez la fonction [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) pour énumérer les produits enregistrés avec le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="598f9-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="598f9-123">Appelez la fonction [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) pour énumérer les composants.</span><span class="sxs-lookup"><span data-stu-id="598f9-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="598f9-124">Appelez la fonction [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) pour énumérer les qualificateurs de composants.</span><span class="sxs-lookup"><span data-stu-id="598f9-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="598f9-125">Appelez la fonction [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) pour énumérer les produits pour un composant particulier.</span><span class="sxs-lookup"><span data-stu-id="598f9-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="598f9-126">Si la valeur de retour d’une fonction d’énumération est une erreur de \_ réussite, il y a encore plus d’éléments à énumérer et la fonction doit être appelée à nouveau avec une variable d’index incrémentée.</span><span class="sxs-lookup"><span data-stu-id="598f9-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="598f9-127">Si la valeur de retour est \_ \_ une erreur plus aucun \_ élément, tous les éléments ont été énumérés et la fonction ne doit pas être rappelée.</span><span class="sxs-lookup"><span data-stu-id="598f9-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



