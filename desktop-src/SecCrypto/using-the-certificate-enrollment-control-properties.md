---
description: Chaque propriété de contrôle d’inscription de certificat est en lecture/écriture et a une valeur par défaut initialisée, ainsi qu’un ensemble de valeurs acceptables.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Utilisation des propriétés du contrôle d’inscription de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753436"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="d72d4-103">Utilisation des propriétés du contrôle d’inscription de certificat</span><span class="sxs-lookup"><span data-stu-id="d72d4-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="d72d4-104">Chaque propriété de contrôle d’inscription de certificat est en lecture/écriture et a une valeur par défaut initialisée, ainsi qu’un ensemble de valeurs acceptables.</span><span class="sxs-lookup"><span data-stu-id="d72d4-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="d72d4-105">Vous pouvez définir une propriété sur n’importe quelle valeur dans cet ensemble afin de modifier le comportement des méthodes qui utilisent la propriété.</span><span class="sxs-lookup"><span data-stu-id="d72d4-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="d72d4-106">Pour obtenir un comportement souhaité, définissez la propriété avant d’appeler la méthode qui utilise la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d72d4-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="d72d4-107">Notez, toutefois, qu’après l’appel des méthodes suivantes</span><span class="sxs-lookup"><span data-stu-id="d72d4-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="d72d4-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="d72d4-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="d72d4-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="d72d4-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="d72d4-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="d72d4-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="d72d4-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="d72d4-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="d72d4-112">la réinitialisation des propriétés suivantes est bloquée</span><span class="sxs-lookup"><span data-stu-id="d72d4-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="d72d4-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="d72d4-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="d72d4-114">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="d72d4-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="d72d4-115">**ProviderFlags**</span><span class="sxs-lookup"><span data-stu-id="d72d4-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="d72d4-116">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="d72d4-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="d72d4-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d72d4-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="d72d4-118">à moins que la méthode [**ICEnroll4 :: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="d72d4-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="d72d4-119">Pour plus d’informations sur les propriétés et les méthodes individuelles, consultez les rubriques de référence pour ces propriétés et méthodes dans la [référence de chiffrement](cryptography-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d72d4-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="d72d4-120">Les sections suivantes contiennent des informations spécifiques à la langue pour la définition et la récupération des propriétés du contrôle d’inscription de certificat :</span><span class="sxs-lookup"><span data-stu-id="d72d4-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="d72d4-121">Propriétés du contrôle d’inscription de certificat en C++</span><span class="sxs-lookup"><span data-stu-id="d72d4-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
