---
description: La documentation suivante est valide uniquement lorsque Digest est utilisé en tant que mécanisme SASL. Les chiffrements et le chiffrement ne sont pas disponibles pour l’authentification HTTP à l’aide de Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Chiffrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202197"
---
# <a name="ciphers"></a><span data-ttu-id="e4f74-104">Chiffrements</span><span class="sxs-lookup"><span data-stu-id="e4f74-104">Ciphers</span></span>

<span data-ttu-id="e4f74-105">La documentation suivante est valide uniquement lorsque Digest est utilisé en tant que mécanisme SASL.</span><span class="sxs-lookup"><span data-stu-id="e4f74-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="e4f74-106">Les chiffrements et le chiffrement ne sont pas disponibles pour l’authentification HTTP à l’aide de Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="e4f74-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="e4f74-107">La directive de chiffrement d’un challenge SASL Digest contient une liste des chiffrements pris en charge par un serveur nécessitant des communications confidentielles.</span><span class="sxs-lookup"><span data-stu-id="e4f74-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="e4f74-108">La directive de chiffrement ne peut être incluse que si la directive QoP a la valeur « auth-CONF ».</span><span class="sxs-lookup"><span data-stu-id="e4f74-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="e4f74-109">Les chiffrements reconnus par Microsoft Digest sont répertoriés dans le tableau suivant, dans l’ordre, de la plus forte à la plus faible.</span><span class="sxs-lookup"><span data-stu-id="e4f74-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="e4f74-110">Valeur de chiffrement</span><span class="sxs-lookup"><span data-stu-id="e4f74-110">Cipher value</span></span> | <span data-ttu-id="e4f74-111">Description</span><span class="sxs-lookup"><span data-stu-id="e4f74-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f74-112">RC4</span><span class="sxs-lookup"><span data-stu-id="e4f74-112">"rc4"</span></span>        | <span data-ttu-id="e4f74-113">Le chiffrement RC4 avec une clé de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="e4f74-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e4f74-114">alors</span><span class="sxs-lookup"><span data-stu-id="e4f74-114">"3des"</span></span>       | <span data-ttu-id="e4f74-115">Le chiffrement [*triple des*](/windows/desktop/SecGloss/t-gly) en mode [*CBC*](/windows/desktop/SecGloss/c-gly) avec Ede avec la même clé pour chaque étape E (mode à deux clés).</span><span class="sxs-lookup"><span data-stu-id="e4f74-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="e4f74-116">La longueur totale de la clé est de 112 bits.</span><span class="sxs-lookup"><span data-stu-id="e4f74-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="e4f74-117">« RC4-56 »</span><span class="sxs-lookup"><span data-stu-id="e4f74-117">"rc4-56"</span></span>     | <span data-ttu-id="e4f74-118">Le chiffrement RC4 avec une clé de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="e4f74-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e4f74-119">« RC4-40 »</span><span class="sxs-lookup"><span data-stu-id="e4f74-119">"rc4-40"</span></span>     | <span data-ttu-id="e4f74-120">Le chiffrement RC4 avec une clé de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="e4f74-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e4f74-121">des</span><span class="sxs-lookup"><span data-stu-id="e4f74-121">"des"</span></span>        | <span data-ttu-id="e4f74-122">Le chiffrement des ( [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) ) dans le mode de [*chaînage de blocs de chiffrement*](/windows/desktop/SecGloss/c-gly) (CBC) avec une clé de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="e4f74-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="e4f74-123">Quand une application serveur demande la confidentialité (QoP = "auth-conf") Microsoft Digest génère une stimulation qui offre au client tous les chiffrements installés sur le serveur et pris en charge par le Digest.</span><span class="sxs-lookup"><span data-stu-id="e4f74-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="e4f74-124">Le client Digest sélectionne le chiffrement le plus élevé disponible.</span><span class="sxs-lookup"><span data-stu-id="e4f74-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="e4f74-125">Pour plus d’informations sur la spécification de la confidentialité, consultez [génération de la demande de résumé](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="e4f74-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
