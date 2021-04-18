---
title: Connexions à liaisons multiples et rappels
description: Pour le premier lien d’une connexion à liaisons multiples, le service d’authentification définit l’indicateur de lien d’abord de l’indicateur EAP d’accès distant \_ \_ \_ \_ dans le membre fFlags de la \_ \_ structure d’entrée EAP PPP.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106509631"
---
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="ede27-103">Connexions à liaisons multiples et rappels</span><span class="sxs-lookup"><span data-stu-id="ede27-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="ede27-104">Pour le premier lien d’une connexion à liaisons multiples, le service d’authentification définit l’indicateur de lien d’abord de l’indicateur EAP d’accès distant \_ \_ \_ \_ dans le membre **fFlags** de la structure [**\_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) .</span><span class="sxs-lookup"><span data-stu-id="ede27-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="ede27-105">Le protocole d’authentification peut utiliser la présence de cet indicateur pour déterminer s’il faut présenter une interface utilisateur spécifiquement pour le premier lien d’une connexion à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="ede27-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="ede27-106">Si la connexion est configurée de sorte que le serveur rappelle l’ordinateur client, l' \_ indicateur d’abord de l’indicateur EAP EAP n’est \_ \_ \_ pas défini sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="ede27-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="ede27-107">Si le protocole d’authentification affecte la **valeur true** au membre **fSaveConnectionData** de la [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) , les liens suivants de la connexion multilien reçoivent les nouvelles données spécifiques à la connexion.</span><span class="sxs-lookup"><span data-stu-id="ede27-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="ede27-108">Toutefois, dans le cas de données spécifiques à l’utilisateur, le protocole d’authentification continue à récupérer les données d’origine propres à l’utilisateur, même s’il affecte la **valeur true** au membre **fSaveUserData** de la **\_ \_ sortie EAP PPP** .</span><span class="sxs-lookup"><span data-stu-id="ede27-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="ede27-109">Le protocole d’authentification peut utiliser une [interface utilisateur interactive](interactive-user-interface.md) pour collecter des données pour un lien spécifique d’une connexion à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="ede27-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="ede27-110">Dans ce cas, le service d’authentification rend les données obtenues disponibles au protocole d’authentification lors des liens suivants.</span><span class="sxs-lookup"><span data-stu-id="ede27-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="ede27-111">Toutefois, ces données ne sont jamais enregistrées dans un stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="ede27-111">However, this data is never saved to persistent storage.</span></span>

 

 




