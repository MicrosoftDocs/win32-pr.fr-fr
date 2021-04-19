---
description: Limitations de sécurité en mode groupe de travail
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitations de sécurité en mode groupe de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517192"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="bb859-103">Limitations de sécurité en mode groupe de travail</span><span class="sxs-lookup"><span data-stu-id="bb859-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="bb859-104">La configuration du groupe de travail [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) n’autorise pas le service composants en file d’attente com+ à prendre en charge la sécurité de l’application.</span><span class="sxs-lookup"><span data-stu-id="bb859-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="bb859-105">Si vous avez installé Message Queuing avec la configuration du groupe de travail, vous devez [désactiver la sécurité](specifying-the-authentication-protocol.md) sur chaque application en file d’attente accessible dans cette configuration en sélectionnant **ne pas authentifier les messages** **sous l’onglet mise en file d'** attente de la boîte de dialogue des **Propriétés** de l’application com+, à l’aide de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="bb859-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="bb859-106">Cette opération ne doit être effectuée que sur un réseau approuvé et doit être effectuée au niveau du client et du serveur si l’application a déjà été exportée.</span><span class="sxs-lookup"><span data-stu-id="bb859-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



