---
title: Création d’une référence externe
description: Si un objet crossRef externe est créé et qu’un contrôleur de domaine l’utilise pour générer une référence, l’objet crossRef fournit deux éléments de données importants dans les propriétés suivantes.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- références externes Active Directory
- Active Directory exemples Active Directory, création d’une référence externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724589"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="cbd0c-105">Création d’une référence externe</span><span class="sxs-lookup"><span data-stu-id="cbd0c-105">Creating an External Referral</span></span>

<span data-ttu-id="cbd0c-106">Si un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) externe est créé et qu’un contrôleur de domaine l’utilise pour générer une référence, l’objet **crossRef** fournit deux éléments de données importants dans les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="cbd0c-107">Pour plus d’informations sur les situations où cela peut se produire, consultez la section précédente.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="cbd0c-108">Propriété</span><span class="sxs-lookup"><span data-stu-id="cbd0c-108">Property</span></span>                           | <span data-ttu-id="cbd0c-109">Description</span><span class="sxs-lookup"><span data-stu-id="cbd0c-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbd0c-110">**dnsRoot**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="cbd0c-111">Spécifie le serveur ou le domaine qui peut fournir des données à partir du contexte d’appellation spécifié dans [**NCName**](/windows/desktop/ADSchema/a-ncname).</span><span class="sxs-lookup"><span data-stu-id="cbd0c-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="cbd0c-112">**nCName**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="cbd0c-113">Spécifie le nom unique pour le domaine, le schéma ou le conteneur de configuration enraciné sur le serveur ou le domaine spécifié par [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot).</span><span class="sxs-lookup"><span data-stu-id="cbd0c-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="cbd0c-114">Par exemple, si le serveur avec l’adresse DNS serv1.northwest.Fabrikam.com sert de contexte d’appellation racine à CN = MyContainer, OU = MyDOM, O = Fabrikam, définissez le [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot) sur l’adresse DNS de ce serveur et le [**NCName**](/windows/desktop/ADSchema/a-ncname) sur le nom unique du domaine, du schéma ou du conteneur de configuration.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="cbd0c-115">Pour plus d’informations et pour obtenir un exemple de code qui montre comment créer une référence externe, consultez l' [exemple de code pour la création d’un objet crossRef externe](example-code-for-creating-an-external-crossref-object.md).</span><span class="sxs-lookup"><span data-stu-id="cbd0c-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 