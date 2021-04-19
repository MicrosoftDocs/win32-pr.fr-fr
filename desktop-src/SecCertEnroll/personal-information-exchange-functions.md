---
description: Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll pour gérer les messages d’échange d’informations personnelles (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Fonctions d’échange d’informations personnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540883"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="c4068-103">Fonctions d’échange d’informations personnelles</span><span class="sxs-lookup"><span data-stu-id="c4068-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="c4068-104">Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll pour gérer les messages d’échange d’informations personnelles (PFX).</span><span class="sxs-lookup"><span data-stu-id="c4068-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="c4068-105">Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="c4068-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="c4068-106">createFilePFXWStr</span><span class="sxs-lookup"><span data-stu-id="c4068-106">createFilePFXWStr</span></span>

<span data-ttu-id="c4068-107">La fonction [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) dans Xenroll.dll enregistre une chaîne de certificats et une [*clé privée*](/windows/desktop/SecGloss/p-gly) dans un fichier à l’aide du format pfx.</span><span class="sxs-lookup"><span data-stu-id="c4068-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="c4068-108">La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités permettant de copier le message PFX dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c4068-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="c4068-109">Toutefois, vous pouvez utiliser la méthode [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sur l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour créer un message pfx encodé et écrire une fonction personnalisée pour enregistrer le message dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c4068-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="c4068-110">createPFXWStr</span><span class="sxs-lookup"><span data-stu-id="c4068-110">createPFXWStr</span></span>

<span data-ttu-id="c4068-111">La fonction [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) dans Xenroll.dll enregistre une chaîne de certificats et une clé privée dans une chaîne de format pfx.</span><span class="sxs-lookup"><span data-stu-id="c4068-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="c4068-112">Vous pouvez utiliser la méthode [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sur l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour créer un message pfx encodé contenant la chaîne et la clé de certificat.</span><span class="sxs-lookup"><span data-stu-id="c4068-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="c4068-113">Vous pouvez spécifier un mot de passe, des options d’exportation et un type de codage.</span><span class="sxs-lookup"><span data-stu-id="c4068-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="c4068-114">Pour récupérer une chaîne qui est équivalente à celle retournée à partir de [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), transmettez l' \_ indicateur binaire XCN crypto \_ String \_ dans le dans le paramètre *Encoding* de la méthode [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .</span><span class="sxs-lookup"><span data-stu-id="c4068-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4068-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4068-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4068-116">Mappage de Xenroll.dll à CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="c4068-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="c4068-117">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="c4068-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
