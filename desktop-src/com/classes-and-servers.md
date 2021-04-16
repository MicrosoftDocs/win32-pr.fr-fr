---
title: Classes et serveurs
description: Classes et serveurs
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382964"
---
# <a name="classes-and-servers"></a><span data-ttu-id="c3ee8-103">Classes et serveurs</span><span class="sxs-lookup"><span data-stu-id="c3ee8-103">Classes and Servers</span></span>

<span data-ttu-id="c3ee8-104">COM utilise **la \_ \_ racine de classes HKEY** pour les paramètres au niveau de l’ordinateur, mais permet également une configuration par utilisateur des CLSID pour une sécurité et une flexibilité accrues.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="c3ee8-105">COM First consulte les classes de logiciels de l' **\_ \_ utilisateur \\ \\ actuel HKEY** avant d’examiner la **\_ \_ racine des classes HKEY**.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="c3ee8-106">COM conserve les informations sur l’ordinateur relatives aux CLSID sous **le \_ \_ \\ CLSID racine** de la classe HKEY et conserve les informations de classe par utilisateur sous **HKEY \_ Current \_ User \\ Software \\ classes \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="c3ee8-107">Les serveurs COM prennent en charge l’inscription automatique.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-107">COM servers support self-registration.</span></span> <span data-ttu-id="c3ee8-108">Pour un serveur in-process, cela signifie que la DLL doit exporter les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3ee8-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="c3ee8-109">**Accompli**</span><span class="sxs-lookup"><span data-stu-id="c3ee8-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="c3ee8-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="c3ee8-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="c3ee8-111">Vous devez exporter explicitement ces fonctions à l’aide d’un fichier de définition de module, de commutateurs de l’éditeur de liens ou de directives de compilateur.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="c3ee8-112">Le magasin de classes utilise ces fonctions pour configurer le registre local après le téléchargement du fichier sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="c3ee8-113">En plus de la Banque de classes, ces fonctions sont également utilisées par d’autres environnements pour installer des serveurs sur des ordinateurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="c3ee8-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3ee8-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3ee8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3ee8-115">Inscription des applications COM</span><span class="sxs-lookup"><span data-stu-id="c3ee8-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 