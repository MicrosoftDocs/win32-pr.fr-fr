---
description: Les exemples de programmes dans les sections suivantes effectuent des opérations qui requièrent que les paires de clés publique/privée soient disponibles pour le chiffrement et le déchiffrement des fichiers, des messages et des signatures.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Conteneurs de clés, clés et certificats nécessaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759465"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="e90d0-103">Conteneurs de clés, clés et certificats nécessaires</span><span class="sxs-lookup"><span data-stu-id="e90d0-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="e90d0-104">Les exemples de programmes dans les sections suivantes effectuent des opérations qui requièrent que les [*paires de clés publique/privée*](../secgloss/p-gly.md) soient disponibles pour le chiffrement et le déchiffrement des fichiers, des messages et des signatures.</span><span class="sxs-lookup"><span data-stu-id="e90d0-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="e90d0-105">La plupart de ces programmes se compilent, se lient et s’exécutent mais échouent au moment de l’exécution sans l’existence de [*conteneurs de clés*](../secgloss/k-gly.md), de clés, de [*magasins de certificats*](../secgloss/c-gly.md)et de certificats appropriés dans ces magasins.</span><span class="sxs-lookup"><span data-stu-id="e90d0-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="e90d0-106">En outre, certains des certificats du magasin MY doivent avoir certaines de leurs propriétés étendues définies.</span><span class="sxs-lookup"><span data-stu-id="e90d0-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="e90d0-107">La création du conteneur de clé par défaut nécessaire peut être effectuée en exécutant le programme dans l' [exemple de programme C : création d’un conteneur de clé et génération de clés](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="e90d0-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="e90d0-108">Notez que la création d’un conteneur de clé ne génère pas automatiquement de paires de clés publiques/privées.</span><span class="sxs-lookup"><span data-stu-id="e90d0-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="e90d0-109">L’exemple de programme, cependant, crée le conteneur de clé et génère les paires de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="e90d0-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="e90d0-110">Une fois les paires de clés publiques/privées générées, vous pouvez obtenir des certificats de test à l’aide d’une [*autorité de certification*](../secgloss/c-gly.md) (ca).</span><span class="sxs-lookup"><span data-stu-id="e90d0-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="e90d0-111">Plusieurs programmes supposent que les certificats avec des noms d’objet spécifiques existent dans le magasin mon système.</span><span class="sxs-lookup"><span data-stu-id="e90d0-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="e90d0-112">En particulier, plusieurs programmes recherchent les certificats dont le nom d’objet est « certificat de test complet » et « Hortense ».</span><span class="sxs-lookup"><span data-stu-id="e90d0-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="e90d0-113">Les noms de sujet des certificats peuvent être modifiés dans le code pour correspondre aux noms de sujet des certificats qui existent dans le magasin de certificats MY.</span><span class="sxs-lookup"><span data-stu-id="e90d0-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="e90d0-114">L’exécution de l’exemple de programme dans l' [exemple de programme C : la liste des certificats dans un magasin](example-c-program-listing-the-certificates-in-a-store.md) affiche tous les certificats dans un magasin et toutes les propriétés étendues qui sont définies sur ces certificats.</span><span class="sxs-lookup"><span data-stu-id="e90d0-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
