---
title: Publication avec l’inscription Windows Sockets & résolution
description: Les services Windows Sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services et Rechercher des services publiés avec RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Inscription et résolution Windows Sockets Active Directory, publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "104462631"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="a61e5-104">Publication avec l’inscription Windows Sockets & résolution</span><span class="sxs-lookup"><span data-stu-id="a61e5-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="a61e5-105">Les services Windows Sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services et Rechercher des services publiés avec RnR.</span><span class="sxs-lookup"><span data-stu-id="a61e5-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="a61e5-106">La publication RnR se produit en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="a61e5-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="a61e5-107">La première étape installe une classe de service qui associe un GUID à un nom pour le service.</span><span class="sxs-lookup"><span data-stu-id="a61e5-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="a61e5-108">La classe de service peut contenir des données de configuration spécifiques au service.</span><span class="sxs-lookup"><span data-stu-id="a61e5-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="a61e5-109">Les services peuvent ensuite se publier eux-mêmes en tant qu’instances de la classe de service.</span><span class="sxs-lookup"><span data-stu-id="a61e5-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="a61e5-110">Une fois publiées, les clients peuvent interroger le service d’annuaire pour les instances d’une classe donnée à l’aide des API RnR et sélectionner une instance à lier.</span><span class="sxs-lookup"><span data-stu-id="a61e5-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="a61e5-111">Quand une classe n’est plus nécessaire, elle peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="a61e5-111">When a class is no longer required, it can be removed.</span></span>

 

 




