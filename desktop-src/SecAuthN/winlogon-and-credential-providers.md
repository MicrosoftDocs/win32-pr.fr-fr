---
description: Est le module Windows qui effectue une ouverture de session interactive pour une ouverture de session. Le comportement de Winlogon peut être personnalisé en implémentant et en inscrivant un fournisseur d’informations d’identification.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon et fournisseurs d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951117"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="65b18-104">Winlogon et fournisseurs d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="65b18-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="65b18-105">[*Winlogon*](../secgloss/w-gly.md) est le module Windows qui effectue une ouverture de session interactive pour une [*ouverture de session*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="65b18-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="65b18-106">Le comportement de Winlogon peut être personnalisé en implémentant et en inscrivant un fournisseur d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="65b18-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="65b18-107">Pour plus d’informations sur l’implémentation d’un fournisseur d’informations d’identification, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="65b18-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="65b18-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="65b18-108">Topic</span></span>                                                                                                           | <span data-ttu-id="65b18-109">Description</span><span class="sxs-lookup"><span data-stu-id="65b18-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65b18-110">Expérience d’ouverture de session Windows dirigée par le fournisseur d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="65b18-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="65b18-111">Présentation de Winlogon et de l’architecture du fournisseur d’informations d’identification et d’un exemple de fournisseur d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="65b18-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="65b18-112">Interfaces Shell</span><span class="sxs-lookup"><span data-stu-id="65b18-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="65b18-113">Référence de l’interface du fournisseur d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="65b18-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="65b18-114">Fournisseurs d’informations d’identification dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="65b18-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="65b18-115">Fournisseurs d’informations d’identification tiers et fournisseurs d’informations d’identification système dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="65b18-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="65b18-116">Pour obtenir un exemple d’implémentation de fournisseur d’informations d’identification, consultez l’exemple situé dans le répertoire d’installation de SDK Windows sous \\ exemples de \\ sécurité \\ CredentialProvider.</span><span class="sxs-lookup"><span data-stu-id="65b18-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="65b18-117">**Windows Server 2003 et Windows XP :** Les fournisseurs d’informations d’identification ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="65b18-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="65b18-118">Pour plus d’informations sur la personnalisation de Winlogon, consultez [Winlogon et Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="65b18-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
