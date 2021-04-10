---
description: API voisinage immédiat
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: API voisinage immédiat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952030"
---
# <a name="people-near-me-apis"></a><span data-ttu-id="5af14-103">API voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="5af14-103">People Near Me APIs</span></span>

<span data-ttu-id="5af14-104">Toutes les applications capables de voisinage [immédiat](about-people-near-me.md) (PNM) peuvent utiliser les API Win32 suivantes :</span><span class="sxs-lookup"><span data-stu-id="5af14-104">Any applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following Win32 APIs:</span></span>

### <a name="contacts-api"></a><span data-ttu-id="5af14-105">API contacts</span><span class="sxs-lookup"><span data-stu-id="5af14-105">Contacts API</span></span>

<span data-ttu-id="5af14-106">L’API contacts permet d’accéder aux informations de contact de l’utilisateur connecté, de récupérer des informations sur les contacts précédemment stockés ou de stocker les informations de contact et le certificat numérique d’un nouveau contact.</span><span class="sxs-lookup"><span data-stu-id="5af14-106">The Contacts API is used to access the contact information for the logged on user, retrieve information about previously stored contacts, or store the contact information and digital certificate of a new contact.</span></span>

### <a name="people-near-me-api"></a><span data-ttu-id="5af14-107">API voisinage immédiat</span><span class="sxs-lookup"><span data-stu-id="5af14-107">People Near Me API</span></span>

<span data-ttu-id="5af14-108">L’API PNM est utilisée pour rechercher les utilisateurs à proximité, leurs centres d’intérêt publiés, les objets arbitraires qu’ils choisissent de publier et les applications publiées.</span><span class="sxs-lookup"><span data-stu-id="5af14-108">The PNM API is used to find users nearby, their advertised interests, any arbitrary objects they choose to publish, and advertised applications.</span></span>

### <a name="publication-api"></a><span data-ttu-id="5af14-109">API de publication</span><span class="sxs-lookup"><span data-stu-id="5af14-109">Publication API</span></span>

<span data-ttu-id="5af14-110">L’API de publication est utilisée pour interagir avec les contacts distants.</span><span class="sxs-lookup"><span data-stu-id="5af14-110">The Publication API is used to interact with remote contacts.</span></span> <span data-ttu-id="5af14-111">La couche de [signalisation d’homologue](windows-peer-components-for-people-near-me.md) utilisée par le gestionnaire de publication est également utilisée par le module PNM pour établir des connexions.</span><span class="sxs-lookup"><span data-stu-id="5af14-111">The [Peer Signaling](windows-peer-components-for-people-near-me.md) layer used by the Publication Manager is also used by the PNM module for establishing connections.</span></span>

### <a name="invitation-api"></a><span data-ttu-id="5af14-112">API d’invitation</span><span class="sxs-lookup"><span data-stu-id="5af14-112">Invitation API</span></span>

<span data-ttu-id="5af14-113">L’API d’invitation est utilisée par une application de collaboration pour inviter un ou plusieurs homologues spécifiques dans une activité de collaboration.</span><span class="sxs-lookup"><span data-stu-id="5af14-113">The Invitation API is used by a collaboration application to invite specific peer(s) into a collaboration activity.</span></span>

### <a name="application-registration-api"></a><span data-ttu-id="5af14-114">API d’inscription des applications</span><span class="sxs-lookup"><span data-stu-id="5af14-114">Application Registration API</span></span>

<span data-ttu-id="5af14-115">L’API d’inscription d’application est utilisée par le programme d’installation d’une application de collaboration pour inscrire l’application.</span><span class="sxs-lookup"><span data-stu-id="5af14-115">The Application Registration API is used by the installer of a collaboration application to register the application.</span></span> <span data-ttu-id="5af14-116">Une application qui prend en charge PNM demandera à l’utilisateur pendant le processus d’installation de déterminer si l’application doit être mise à la disposition des utilisateurs sur le sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5af14-116">A PNM-capable application will prompt the user during the installation process to determine whether the application should be made available to users on the subnet.</span></span>

 

 



