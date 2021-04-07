---
description: Vous pouvez écrire des modules de stratégie dans le langage de programmation C, C++ ou Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Écriture de modules personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952113"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="036d1-103">Écriture de modules personnalisés</span><span class="sxs-lookup"><span data-stu-id="036d1-103">Writing Custom Modules</span></span>

<span data-ttu-id="036d1-104">Vous pouvez écrire des modules de stratégie dans le langage de programmation C, C++ ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="036d1-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="036d1-105">Le compilateur Microsoft requis est disponible dans Visual C++ version 5,0 ou ultérieure, ou dans Visual Basic version 5,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="036d1-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="036d1-106">Une [*autorité de certification*](../secgloss/c-gly.md) d’entreprise (ca) doit utiliser uniquement le module de stratégie d’entreprise fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="036d1-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="036d1-107">Vous devez implémenter [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) lors de l’écriture d’un module de stratégie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="036d1-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="036d1-108">En outre, vous devez implémenter [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) lors de l’écriture d’un module de stratégie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="036d1-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="036d1-109">Les modules de stratégie peuvent appeler des méthodes à partir de [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) pour faciliter le traitement d’une [*demande de certificat*](../secgloss/c-gly.md); **ICertServerPolicy** permet de définir et d’extraire des propriétés et des extensions de certificat.</span><span class="sxs-lookup"><span data-stu-id="036d1-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="036d1-110">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="036d1-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="036d1-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="036d1-111">Topic</span></span>                                                                      | <span data-ttu-id="036d1-112">Description</span><span class="sxs-lookup"><span data-stu-id="036d1-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="036d1-113">Définition des propriétés d’un certificat</span><span class="sxs-lookup"><span data-stu-id="036d1-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="036d1-114">Définition des propriétés d’un certificat</span><span class="sxs-lookup"><span data-stu-id="036d1-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="036d1-115">Écriture de modules de sortie personnalisés</span><span class="sxs-lookup"><span data-stu-id="036d1-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="036d1-116">Écriture de modules de sortie personnalisés</span><span class="sxs-lookup"><span data-stu-id="036d1-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="036d1-117">Écriture de gestionnaires d’extensions personnalisés</span><span class="sxs-lookup"><span data-stu-id="036d1-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="036d1-118">Écriture de gestionnaires d’extensions personnalisés</span><span class="sxs-lookup"><span data-stu-id="036d1-118">Writing custom extension handlers</span></span>       |



 

 

 
