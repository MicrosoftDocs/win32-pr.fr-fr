---
description: L’application d’une règle de codage aux structures de données décrites par une syntaxe abstraite fournit une syntaxe de transfert qui régit la façon dont les octets d’un flux sont organisés lorsqu’ils sont envoyés entre les ordinateurs.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Syntaxe de transfert DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565032"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="79ffe-103">Syntaxe de transfert DER</span><span class="sxs-lookup"><span data-stu-id="79ffe-103">DER Transfer Syntax</span></span>

<span data-ttu-id="79ffe-104">L’application d’une règle de codage aux structures de données décrites par une syntaxe abstraite fournit une syntaxe de transfert qui régit la façon dont les octets d’un flux sont organisés lorsqu’ils sont envoyés entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="79ffe-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="79ffe-105">La syntaxe de transfert utilisée par Distinguished Encoding Rules suit toujours un format de *balise, de longueur et de valeur* .</span><span class="sxs-lookup"><span data-stu-id="79ffe-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="79ffe-106">Le format est généralement désigné sous le terme de triplet TLV dans lequel chaque champ (T, L ou V) contient un ou plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="79ffe-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![type der, longueur et valeur (TLV) triplet](images/der-tlv-basic.png)

<span data-ttu-id="79ffe-108">Le champ de *balise* spécifie le type de la structure de données à envoyer, le champ de *longueur* spécifie le nombre d’octets de contenu à transférer et le champ de *valeur* contient le contenu.</span><span class="sxs-lookup"><span data-stu-id="79ffe-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="79ffe-109">Notez que le champ *valeur* peut être un triplet s’il contient un type de données construit comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="79ffe-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![récursivité des triplets de der TLV](images/der-tlv-recursive.png)

<span data-ttu-id="79ffe-111">Consultez les rubriques suivantes pour obtenir des informations détaillées sur les composants d’un tripleon.</span><span class="sxs-lookup"><span data-stu-id="79ffe-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="79ffe-112">Octets de balise encodés</span><span class="sxs-lookup"><span data-stu-id="79ffe-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="79ffe-113">Octets de longueur et de valeur encodés</span><span class="sxs-lookup"><span data-stu-id="79ffe-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="79ffe-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79ffe-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79ffe-115">Types construits</span><span class="sxs-lookup"><span data-stu-id="79ffe-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="79ffe-116">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="79ffe-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



