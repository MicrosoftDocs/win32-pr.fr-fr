---
title: Fonctions d’autorisation (RPC)
description: Chaque fois qu’un programme serveur reçoit une demande client pour accéder à l’une des procédures distantes de gestion, la bibliothèque Runtime RPC appelle une fonction d’autorisation par défaut.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104030544"
---
# <a name="authorization-functions"></a><span data-ttu-id="89663-103">Fonctions d’autorisation</span><span class="sxs-lookup"><span data-stu-id="89663-103">Authorization Functions</span></span>

<span data-ttu-id="89663-104">Chaque fois qu’un programme serveur reçoit une demande client pour accéder à l’une des procédures distantes de gestion, la bibliothèque Runtime RPC appelle une fonction d’autorisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="89663-104">Each time a server program receives a client request for access to one of the management remote procedures, the RPC run-time library invokes a default authorization function.</span></span> <span data-ttu-id="89663-105">Cette fonction utilise le SSP pour vérifier les informations d’identification du client et autoriser ou rejeter la demande.</span><span class="sxs-lookup"><span data-stu-id="89663-105">This function uses the SSP to check the client's credentials and authorize or reject the request.</span></span>

<span data-ttu-id="89663-106">Votre programme serveur peut remplacer la fonction d’autorisation fournie par le fournisseur de services partagés.</span><span class="sxs-lookup"><span data-stu-id="89663-106">Your server program can override the authorization function that the SSP provides.</span></span> <span data-ttu-id="89663-107">Appelez la fonction [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) et transmettez-la à l’adresse de votre fonction d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="89663-107">Invoke the function [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) and pass it to the address of your authorization function.</span></span> <span data-ttu-id="89663-108">Une fois que le programme serveur a défini la fonction d’autorisation, la bibliothèque Runtime RPC l’appelle chaque fois que le programme serveur reçoit une demande du client pour l’une des fonctions de gestion.</span><span class="sxs-lookup"><span data-stu-id="89663-108">Once the server program sets the authorization function, the RPC run-time library calls it every time the server program receives a client request to one of the management functions.</span></span> <span data-ttu-id="89663-109">Pour plus d’informations, consultez [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)et [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span><span class="sxs-lookup"><span data-stu-id="89663-109">For more information, see [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname), and [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span></span>

 

 




