---
description: Exemple de certificat. Créer des applications pour la certification d’API, installer un certificat SSL, un certificat de serveur, créer un certificat sur un support, tel qu’Internet ou un intranet, qui ne sont pas sécurisés par nature.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API d’inscription de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526337"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="ce691-104">API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="ce691-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="ce691-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="ce691-105">Purpose</span></span>

<span data-ttu-id="ce691-106">L’API d’inscription de certificats peut être utilisée pour créer une application cliente afin de demander un certificat et d’installer une réponse de certificat.</span><span class="sxs-lookup"><span data-stu-id="ce691-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="ce691-107">Cette API est implémentée dans CertEnroll.dll à partir de Windows Vista. Il remplace Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="ce691-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ce691-108">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="ce691-108">Developer audience</span></span>

<span data-ttu-id="ce691-109">L’API d’inscription de certificats est destinée aux développeurs d’applications qui permettent aux utilisateurs de créer, de demander et de récupérer des certificats sur des médias, tels qu’Internet ou un intranet, qui ne sont pas sécurisés par nature.</span><span class="sxs-lookup"><span data-stu-id="ce691-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="ce691-110">Les développeurs doivent être familiarisés avec les langages de programmation C et C++, le modèle COM (Component Object Model) et l’environnement de programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="ce691-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="ce691-111">Bien que cela ne soit pas obligatoire, il est recommandé de comprendre le chiffrement et l’infrastructure de clé publique.</span><span class="sxs-lookup"><span data-stu-id="ce691-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ce691-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="ce691-112">Run-time requirements</span></span>

<span data-ttu-id="ce691-113">L’API d’inscription de certificats est prise en charge à partir de Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce691-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="ce691-114">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ce691-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce691-115">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="ce691-115">In this section</span></span>



| <span data-ttu-id="ce691-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ce691-116">Topic</span></span>                                                                                       | <span data-ttu-id="ce691-117">Description</span><span class="sxs-lookup"><span data-stu-id="ce691-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce691-118">À propos de l’API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="ce691-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="ce691-119">Les concepts clés relatifs aux demandes de certificat sont décrits.</span><span class="sxs-lookup"><span data-stu-id="ce691-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="ce691-120">Utilisation de l’API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="ce691-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="ce691-121">Comment utiliser l’API d’inscription de certificats pour étendre les fonctionnalités de Active Directory les services de certificats.</span><span class="sxs-lookup"><span data-stu-id="ce691-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="ce691-122">Référence de l’API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="ce691-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="ce691-123">Description détaillée des interfaces, énumérations et autres éléments de programmation qui peuvent être utilisés pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.</span><span class="sxs-lookup"><span data-stu-id="ce691-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




