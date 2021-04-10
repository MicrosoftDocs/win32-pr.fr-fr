---
description: Le fragment de code suivant illustre la modification d’un intervalle de temps de conférences. L’intervalle de temps par défaut est de trente minutes. Dans ce fragment, l’intervalle de temps est défini sur une année.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modification d’une conférence connue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201205"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="034db-105">Modification d’une conférence connue</span><span class="sxs-lookup"><span data-stu-id="034db-105">Modifying a Known Conference</span></span>

<span data-ttu-id="034db-106">\[Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="034db-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="034db-107">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="034db-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="034db-108">Le fragment de code suivant illustre la modification de l’intervalle de temps d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="034db-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="034db-109">L’intervalle de temps par défaut est de trente minutes.</span><span class="sxs-lookup"><span data-stu-id="034db-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="034db-110">Dans ce fragment, l’intervalle de temps est défini sur une année.</span><span class="sxs-lookup"><span data-stu-id="034db-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="034db-111">Ce fragment suppose que la [connexion à un serveur ils](connecting-to-an-ils-server.md) a déjà été effectuée et qu’une [énumération de répertoires de conférence](enumerating-conference-directories.md) a été effectuée pour obtenir l’entrée d’annuaire qui sera modifiée.</span><span class="sxs-lookup"><span data-stu-id="034db-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="034db-112">Ce fragment suppose également qu’il ne s’agit pas d’une conférence multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="034db-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="034db-113">La modification des heures d’une conférence multidiffusion requiert la notification du serveur d’allocation d’adresses de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="034db-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="034db-114">Pour obtenir un exemple d’utilisation de l’adressage de multidiffusion, consultez [acquisition d’une adresse de multidiffusion](acquiring-a-multicast-address.md) .</span><span class="sxs-lookup"><span data-stu-id="034db-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="034db-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="034db-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="034db-116">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="034db-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



