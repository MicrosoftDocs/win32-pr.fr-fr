---
title: Installation d’EAP
description: Les fournisseurs implémentent EAPs, également appelés protocoles d’authentification, dans les bibliothèques de liens dynamiques (dll).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381269"
---
# <a name="eap-installation"></a><span data-ttu-id="deb33-103">Installation d’EAP</span><span class="sxs-lookup"><span data-stu-id="deb33-103">EAP Installation</span></span>

<span data-ttu-id="deb33-104">Les fournisseurs implémentent EAPs, également appelés protocoles d’authentification, dans les bibliothèques de liens dynamiques (dll).</span><span class="sxs-lookup"><span data-stu-id="deb33-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="deb33-105">Une DLL pour le protocole d’authentification doit résider sur les ordinateurs client et serveur.</span><span class="sxs-lookup"><span data-stu-id="deb33-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="deb33-106">Par souci de simplicité, les dll du client et du serveur peuvent être identiques. Toutefois, cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="deb33-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="deb33-107">Sachez également que la même DLL peut prendre en charge plusieurs protocoles d’authentification.</span><span class="sxs-lookup"><span data-stu-id="deb33-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="deb33-108">Le fournisseur doit fournir un logiciel d’installation pour installer et supprimer la DLL.</span><span class="sxs-lookup"><span data-stu-id="deb33-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="deb33-109">Le logiciel d’installation doit également créer les clés et valeurs appropriées pour le protocole d’authentification dans le registre système, puis les supprimer lors de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="deb33-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="deb33-110">L’installation de chaque DLL EAP doit créer la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="deb33-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="deb33-111">**HKEY \_ LOCAL \_ machine** \\ **System système** \\ **CurrentControlSet** \\ **services** \\ **rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**</span><span class="sxs-lookup"><span data-stu-id="deb33-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="deb33-112">Dans le chemin d’accès précédent, **&lt; eaptypeid &gt;** est l’ID du protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="deb33-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="deb33-113">Le fournisseur doit obtenir cet ID auprès de l’IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="deb33-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="deb33-114">Pour plus d’informations et pour obtenir une description des valeurs prises en charge pour cette clé, consultez [valeurs de Registre du protocole d’authentification](authentication-protocol-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="deb33-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




