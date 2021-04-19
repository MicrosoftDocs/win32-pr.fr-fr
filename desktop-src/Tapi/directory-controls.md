---
description: Le diagramme suivant illustre les principaux objets impliqués dans les contrôles de répertoires TAPI 3 Rendezvous. Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Contrôles de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538853"
---
# <a name="directory-controls"></a><span data-ttu-id="f2aa5-104">Contrôles de répertoire</span><span class="sxs-lookup"><span data-stu-id="f2aa5-104">Directory Controls</span></span>

<span data-ttu-id="f2aa5-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f2aa5-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f2aa5-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f2aa5-107">Le diagramme suivant illustre les principaux objets impliqués dans les contrôles de répertoires TAPI 3 Rendezvous.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="f2aa5-108">Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![interfaces et objets de contrôle d’annuaire Rendezvous](images/renddir.png)

<span data-ttu-id="f2aa5-110">L’interface de contrôle d’annuaire principale est [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), qui doit être créée en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="f2aa5-111">L’objet Rendezvous expose des méthodes pour récupérer des listes de répertoires disponibles et pour créer des répertoires ou des objets d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="f2aa5-112">Un répertoire réside sur un serveur et est une liste d’objets d’annuaire, ainsi que des informations descriptives.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="f2aa5-113">Les méthodes associées à [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) peuvent obtenir des informations associées à l’annuaire dans son ensemble, par exemple s’il s’agit d’un annuaire ils.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="f2aa5-114">Un objet d’annuaire peut représenter une conférence ou un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="f2aa5-115">L’interface [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) fournit des méthodes qui permettent de récupérer ou de modifier des informations génériques sur un objet d’annuaire, telles que l’adresse de numérotation.</span><span class="sxs-lookup"><span data-stu-id="f2aa5-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="f2aa5-116">Les informations relatives aux conférences et aux utilisateurs, telles que l’URL d’une conférence ou le téléphone IP principal d’un utilisateur, sont manipulées par les méthodes fournies dans les interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) et [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .</span><span class="sxs-lookup"><span data-stu-id="f2aa5-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



