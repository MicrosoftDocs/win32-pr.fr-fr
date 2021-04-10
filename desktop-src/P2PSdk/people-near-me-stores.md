---
description: Personnes proches des boutiques
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Personnes proches des boutiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866694"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="a8d5b-103">Personnes proches des boutiques</span><span class="sxs-lookup"><span data-stu-id="a8d5b-103">People Near Me Stores</span></span>

<span data-ttu-id="a8d5b-104">Les applications capables de voisinage [immédiat](about-people-near-me.md) (PNM) peuvent utiliser les banques de données suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8d5b-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="a8d5b-105">Carnet d’adresses Windows</span><span class="sxs-lookup"><span data-stu-id="a8d5b-105">Windows Address Book</span></span>

<span data-ttu-id="a8d5b-106">Le carnet d’adresses Windows stocke les informations sur les contacts et leurs certificats numériques.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="a8d5b-107">Le contact «**me**», représentant l’utilisateur actuellement connecté, est également stocké dans le carnet d’adresses Windows.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="a8d5b-108">Magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="a8d5b-108">Certificate Store</span></span>

<span data-ttu-id="a8d5b-109">Le magasin de certificats contient le certificat auto-signé pour le contact «**me**».</span><span class="sxs-lookup"><span data-stu-id="a8d5b-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="a8d5b-110">Boutique d'applications</span><span class="sxs-lookup"><span data-stu-id="a8d5b-110">Application Store</span></span>

<span data-ttu-id="a8d5b-111">Un programme d’installation d’application inscrit une application avec PNM pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="a8d5b-112">Il s’agit des objets qui peuvent être recherchés par d’autres utilisateurs lorsqu’ils tentent de se connecter à un utilisateur avec une application courante, par exemple un jeu d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="a8d5b-113">Pour chaque application, le magasin d’applications contient le nom de l’application, un identificateur global unique (GUID), une étendue de l’application, une description et un chemin d’accès au fichier exécutable du programme.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="a8d5b-114">L’étendue d’une application peut être définie sur aucun (non publié), voisinage immédiat (publié sur le sous-réseau local), contacts (publiés uniquement pour les contacts) ou tous (publié sur le sous-réseau local et pour les contacts).</span><span class="sxs-lookup"><span data-stu-id="a8d5b-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="a8d5b-115">Le magasin d’applications se trouve dans le Registre Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



