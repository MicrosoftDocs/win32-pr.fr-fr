---
description: L’API de signature numérique XPS permet à un utilisateur de signer un document, de vérifier l’identité du signataire et d’indiquer si un document XPS a été modifié depuis sa signature.
ms.assetid: 8a23617e-92fe-4662-b602-47add5716358
title: API de signature numérique XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c56485a532afbb148e62901c38db49ab81963c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520724"
---
# <a name="xps-digital-signature-api"></a><span data-ttu-id="455e1-103">API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="455e1-103">XPS Digital Signature API</span></span>

<span data-ttu-id="455e1-104">L’API de signature numérique XPS permet à un utilisateur de signer un document, de vérifier l’identité du signataire et d’indiquer si un document XPS a été modifié depuis sa signature.</span><span class="sxs-lookup"><span data-stu-id="455e1-104">The XPS Digital Signature API enables a user to sign a document, verify the identity of the signer, and indicate whether an XPS document has changed since it was signed.</span></span> <span data-ttu-id="455e1-105">L’API de signature numérique XPS repose sur la technologie de signature numérique qui est utilisée dans les conventions Open Packaging, qui sont spécifiées dans la première édition, partie 2, « Open Packaging Conventions » de [Standard ECMA-376, Office Open XML file formats](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span><span class="sxs-lookup"><span data-stu-id="455e1-105">The XPS Digital Signature API is built on the digital signature technology that is used in the Open Packaging Conventions, which are specified in the 1st edition, Part 2, "Open Packaging Conventions," of [Standard ECMA-376, Office Open XML File Formats](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="455e1-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="455e1-106">In This Section</span></span>

<span data-ttu-id="455e1-107">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="455e1-107">This section contains the following topics.</span></span>

### <a name="about-xps-digital-signature-api"></a><span data-ttu-id="455e1-108">À propos de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="455e1-108">About XPS Digital Signature API</span></span>

<span data-ttu-id="455e1-109">À propos de l' [API de signature numérique XPS](about-xps-digital-signatures.md) décrit l’API de signature numérique XPS à un niveau élevé.</span><span class="sxs-lookup"><span data-stu-id="455e1-109">[About XPS Digital Signature API](about-xps-digital-signatures.md) describes the XPS Digital Signature API at a high level.</span></span>

### <a name="using-xps-digital-signature-api"></a><span data-ttu-id="455e1-110">Utilisation de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="455e1-110">Using XPS Digital Signature API</span></span>

<span data-ttu-id="455e1-111">[Utilisation de l’API de signature numérique XPS](using-digital-signatures-in-xps-documents.md) décrit comment utiliser l’API de signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="455e1-111">[Using XPS Digital Signature API](using-digital-signatures-in-xps-documents.md) describes how to use the XPS Digital Signature API.</span></span>

### <a name="xps-digital-signatures-reference"></a><span data-ttu-id="455e1-112">Informations de référence sur les signatures numériques XPS</span><span class="sxs-lookup"><span data-stu-id="455e1-112">XPS Digital Signatures Reference</span></span>

<span data-ttu-id="455e1-113">La [référence de l’API de signature numérique XPS](xps-digital-signatures-programming-reference.md) contient une liste complète des interfaces, des méthodes et des énumérateurs qui sont implémentés par l’API des signatures numériques XPS.</span><span class="sxs-lookup"><span data-stu-id="455e1-113">The [XPS Digital Signature API Reference](xps-digital-signatures-programming-reference.md) contains a complete listing of the interfaces, methods, and enumerators that are implemented by the XPS Digital Signatures API.</span></span>

## <a name="platform-update-for-windows-vista"></a><span data-ttu-id="455e1-114">Mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="455e1-114">Platform Update for Windows Vista</span></span>

<span data-ttu-id="455e1-115">Les interfaces de signature numérique XPS qui sont décrites dans cette section ne sont pas prises en charge par la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="455e1-115">The XPS Digital Signature interfaces that are described in this section are not supported by the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="455e1-116">Une application qui requiert ces interfaces doit s’exécuter sur Windows 7 ou version ultérieure, ou sur Windows Server 2008 R2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="455e1-116">An application that requires these interfaces should run on Windows 7 or later, or on Windows Server 2008 R2 or later.</span></span> <span data-ttu-id="455e1-117">Dans le cas contraire, l’application peut ne pas fournir à l’utilisateur les fonctionnalités complètes de l’application.</span><span class="sxs-lookup"><span data-stu-id="455e1-117">Otherwise, the application may not provide the user with the application's complete functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="455e1-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="455e1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="455e1-119">Packaging</span><span class="sxs-lookup"><span data-stu-id="455e1-119">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="455e1-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="455e1-120">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="455e1-121">Standard ECMA-376, formats de fichier Office Open XML</span><span class="sxs-lookup"><span data-stu-id="455e1-121">Standard ECMA-376, Office Open XML File Formats</span></span>](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
