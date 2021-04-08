---
description: Utilisez les commandes MakeCert pour créer des certificats de test à l’aide des options disponibles avec Internet Explorer version 4,0 ou ultérieure.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Utilisation de MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753445"
---
# <a name="using-makecert"></a><span data-ttu-id="dbb13-103">Utilisation de MakeCert</span><span class="sxs-lookup"><span data-stu-id="dbb13-103">Using MakeCert</span></span>

<span data-ttu-id="dbb13-104">Les exemples suivants utilisent des commandes [Makecert](makecert.md) pour créer des certificats de test à l’aide des options disponibles avec Internet Explorer version 4,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dbb13-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="dbb13-105">Créez un certificat émis par la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="dbb13-106">Enregistrez le certificat dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="dbb13-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="dbb13-107">**Makecert** *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="dbb13-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="dbb13-108">Créez un certificat émis par la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="dbb13-109">Enregistrez-le dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="dbb13-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="dbb13-110">**Makecert-SS** *MyNewStore*</span><span class="sxs-lookup"><span data-stu-id="dbb13-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="dbb13-111">Créez un certificat émis par la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="dbb13-112">Créez un conteneur de clé et enregistrez le certificat dans un magasin et un fichier.</span><span class="sxs-lookup"><span data-stu-id="dbb13-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="dbb13-113">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="dbb13-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="dbb13-114">Créez un certificat émis par la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="dbb13-115">Créez un fichier de clé privée et enregistrez le certificat dans un magasin et dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="dbb13-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="dbb13-116">**Makecert-SV** *MyKeyFile* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="dbb13-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="dbb13-117">Créez un certificat émis par la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="dbb13-118">Créez un conteneur de clé, enregistrez le certificat dans un magasin et dans un fichier, puis rendez la clé privée exportable.</span><span class="sxs-lookup"><span data-stu-id="dbb13-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="dbb13-119">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**</span><span class="sxs-lookup"><span data-stu-id="dbb13-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="dbb13-120">Créez un certificat à l’aide de la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="dbb13-121">Enregistrez le certificat dans un magasin.</span><span class="sxs-lookup"><span data-stu-id="dbb13-121">Save the certificate to a store.</span></span> <span data-ttu-id="dbb13-122">Créez ensuite un autre certificat émis par le certificat créé récemment.</span><span class="sxs-lookup"><span data-stu-id="dbb13-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="dbb13-123">Enregistrez le deuxième certificat dans un autre magasin.</span><span class="sxs-lookup"><span data-stu-id="dbb13-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="dbb13-124">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* **Makecert-is** *MyNewStore* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="dbb13-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="dbb13-125">Créez un certificat à l’aide de la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="dbb13-126">Enregistrez le certificat dans le magasin MY.</span><span class="sxs-lookup"><span data-stu-id="dbb13-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="dbb13-127">Créez ensuite un autre certificat à l’aide du certificat créé récemment.</span><span class="sxs-lookup"><span data-stu-id="dbb13-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="dbb13-128">S’il y a plus d’un certificat dans mon magasin, le certificat doit être identifié à l’aide de son nom commun.</span><span class="sxs-lookup"><span data-stu-id="dbb13-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="dbb13-129">**Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS mon Makecert-est My-in "XXZZYY"-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="dbb13-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="dbb13-130">Créez un certificat à l’aide de la racine de test par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbb13-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="dbb13-131">Enregistrez le certificat dans mon magasin et dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="dbb13-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="dbb13-132">Créez ensuite un autre certificat à l’aide du certificat *MyNew* nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="dbb13-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="dbb13-133">S’il existe plus d’un certificat dans mon magasin, identifiez le premier certificat de manière unique à l’aide du nom du fichier de certificat.</span><span class="sxs-lookup"><span data-stu-id="dbb13-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="dbb13-134">**Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My** *MyNew. cer* **Makecert-is My-IC** *MyNew. cer* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="dbb13-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



