---
description: Le champ de longueur dans un tripleon TLV identifie le nombre d’octets encodés dans le champ de valeur.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Octets de longueur et de valeur encodés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518200"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="95773-103">Octets de longueur et de valeur encodés</span><span class="sxs-lookup"><span data-stu-id="95773-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="95773-104">Le champ de *longueur* dans un tripleon TLV identifie le nombre d’octets encodés dans le champ de *valeur* .</span><span class="sxs-lookup"><span data-stu-id="95773-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="95773-105">Le champ *valeur* contient le contenu envoyé entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="95773-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="95773-106">Si le champ de *valeur* contient moins de 128 octets, le champ de *longueur* ne requiert qu’un octet.</span><span class="sxs-lookup"><span data-stu-id="95773-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="95773-107">Le bit 7 du champ de *longueur* est égal à zéro (0) et les bits restants identifient le nombre d’octets de contenu à envoyer.</span><span class="sxs-lookup"><span data-stu-id="95773-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="95773-108">Si le champ de *valeur* contient plus de 127 octets, le bit 7 du champ de *longueur* est un (1) et les bits restants identifient le nombre d’octets nécessaires pour contenir la longueur.</span><span class="sxs-lookup"><span data-stu-id="95773-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="95773-109">Les exemples sont présentés dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="95773-109">Examples are shown in the following illustration.</span></span>

![octet de longueur der TLV](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="95773-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95773-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95773-112">Syntaxe de transfert DER</span><span class="sxs-lookup"><span data-stu-id="95773-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="95773-113">Octets de balise encodés</span><span class="sxs-lookup"><span data-stu-id="95773-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



