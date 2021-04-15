---
description: À mesure que le nombre de certificats émis dans une infrastructure à clé publique (PKI) augmente, il peut devenir difficile pour une autorité de certification unique d’effectuer un suivi efficace des certificats qu’elle a émis.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Hiérarchie des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561826"
---
# <a name="certificate-hierarchy"></a><span data-ttu-id="a957a-103">Hiérarchie des certificats</span><span class="sxs-lookup"><span data-stu-id="a957a-103">Certificate Hierarchy</span></span>

<span data-ttu-id="a957a-104">À mesure que le nombre de certificats émis dans une infrastructure à clé publique (PKI) augmente, il peut devenir difficile pour une autorité de certification unique d’effectuer un suivi efficace des certificats qu’elle a émis.</span><span class="sxs-lookup"><span data-stu-id="a957a-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="a957a-105">Une façon de résoudre ce problème consiste à créer une hiérarchie de certificats dans laquelle l’autorité de certification délègue l’autorité pour émettre des certificats aux autorités subordonnées qui peuvent, à leur tour, déléguer l’autorité à leurs subordonnés.</span><span class="sxs-lookup"><span data-stu-id="a957a-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="a957a-106">Chaque autorité de certification délègue l’autorité en émettant un certificat d’autorité de certification à un subordonné.</span><span class="sxs-lookup"><span data-stu-id="a957a-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="a957a-107">L’autorité de certification initiale de la chaîne est appelée racine et il n’est pas nécessaire qu’une entité établisse une approbation avec une autorité de certification qui réside sur une [chaîne de certificats](about-certificate-chain.md) différente de celle sur laquelle l’entité réside.</span><span class="sxs-lookup"><span data-stu-id="a957a-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="a957a-108">L’illustration suivante montre une hiérarchie de certificat composée d’une autorité de certification racine, de deux autorités de certification subordonnées à la racine (une pour le service marketing et une pour le service de fabrication) et d’autorités de certification subordonnées à celles-ci.</span><span class="sxs-lookup"><span data-stu-id="a957a-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![diagramme de la hiérarchie des certificats](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="a957a-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a957a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a957a-111">Modèles d’approbation</span><span class="sxs-lookup"><span data-stu-id="a957a-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



