---
description: La syntaxe de message de chiffrement (CMS), dérivée de la \# version 1,5 de PKCS 7, est la syntaxe utilisée pour hacher, signer numériquement, authentifier et chiffrer des messages arbitraires.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Ajouts CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517771"
---
# <a name="cms-additions"></a><span data-ttu-id="59a09-103">Ajouts CMS</span><span class="sxs-lookup"><span data-stu-id="59a09-103">CMS Additions</span></span>

<span data-ttu-id="59a09-104">La syntaxe de message de chiffrement (CMS), dérivée de la \# version 1,5 de PKCS 7, est la syntaxe utilisée pour [*hacher*](../secgloss/h-gly.md), [*signer numériquement*](../secgloss/d-gly.md), authentifier et chiffrer des messages arbitraires.</span><span class="sxs-lookup"><span data-stu-id="59a09-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="59a09-105">Dans la mesure du possible, la compatibilité descendante est préservée. Toutefois, des modifications ont été apportées pour prendre en charge le transfert de certificat d’attribut et les techniques d’accord de clé pour la gestion des clés.</span><span class="sxs-lookup"><span data-stu-id="59a09-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="59a09-106">CMS autorise l’encapsulation multiple afin qu’une enveloppe d’encapsulation puisse être imbriquée dans une autre.</span><span class="sxs-lookup"><span data-stu-id="59a09-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="59a09-107">En outre, une partie peut signer numériquement des données précédemment encapsulées ; des attributs arbitraires, tels que l’heure de signature, peuvent être signés avec le contenu du message ; les attributs et, tels que les contre- [*signatures*](../secgloss/c-gly.md), peuvent être associés à une signature.</span><span class="sxs-lookup"><span data-stu-id="59a09-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="59a09-108">CMS peut prendre en charge diverses architectures pour la gestion des clés basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="59a09-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="59a09-109">Pour prendre en charge des fonctionnalités CMS supplémentaires, de nouveaux champs ont été attribués aux structures de données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="59a09-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="59a09-110">De nouveaux indicateurs et valeurs de paramètre ont également été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="59a09-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="59a09-111">Toutes les structures de données et toutes les API utilisant CMS sont à compatibilité descendante de 100% avec la \# version 1,5 de PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="59a09-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="59a09-112">Les ajouts incluent les ajouts de [données enveloppés](enveloped-data-additions.md) et les [ajouts de données signés](signed-data-additions.md).</span><span class="sxs-lookup"><span data-stu-id="59a09-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
