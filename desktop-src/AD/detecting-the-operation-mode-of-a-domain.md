---
title: Détection du mode d’opération d’un domaine
description: Dans Windows 2000, un domaine peut s’exécuter en deux modes d’opération mixtes et natifs.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Détection du mode d’opération d’un domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842097"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="9bd86-104">Détection du mode d’opération d’un domaine</span><span class="sxs-lookup"><span data-stu-id="9bd86-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="9bd86-105">Dans Windows 2000, un domaine peut s’exécuter en deux modes d’opération : mixte et natif.</span><span class="sxs-lookup"><span data-stu-id="9bd86-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="9bd86-106">Le mode mixte doit être utilisé pour inclure les contrôleurs de domaine exécutant Windows NT 4,0 dans un domaine Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9bd86-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="9bd86-107">Le mode mixte ne prend pas en charge les groupes universels ni les groupes imbriqués.</span><span class="sxs-lookup"><span data-stu-id="9bd86-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="9bd86-108">Si tous les contrôleurs de domaine du domaine exécutent Windows 2000, vous pouvez utiliser le mode natif.</span><span class="sxs-lookup"><span data-stu-id="9bd86-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="9bd86-109">Pour détecter par programme le mode d’opération d’un domaine Windows 2000, lisez la propriété [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) de l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="9bd86-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="9bd86-110">La valeur zéro (0) signifie que le domaine est en mode natif.</span><span class="sxs-lookup"><span data-stu-id="9bd86-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="9bd86-111">La valeur un (1) indique que le domaine est en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="9bd86-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="9bd86-112">Vous pouvez également utiliser la fonction [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) pour obtenir le mode d’opération ainsi que d’autres données sur le domaine et son état.</span><span class="sxs-lookup"><span data-stu-id="9bd86-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="9bd86-113">Pour établir une liaison avec l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) du domaine du compte d’utilisateur sous lequel votre application s’exécute, utilisez une liaison sans serveur et RootDSE pour obtenir le nom unique du domaine, puis utilisez ce nom unique pour établir une liaison à l’objet **domainDNS** qui représente ce domaine.</span><span class="sxs-lookup"><span data-stu-id="9bd86-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="9bd86-114">Pour plus d’informations sur la liaison sans serveur et rootDSE, consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="9bd86-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="9bd86-115">Pour plus d’informations et pour obtenir un exemple de code qui montre comment détecter par programme le mode d’opération d’un domaine, consultez l' [exemple de code permettant de déterminer le mode d’opération](example-code-for-determining-the-operation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="9bd86-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 