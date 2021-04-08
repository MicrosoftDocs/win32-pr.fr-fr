---
title: Affichage des interfaces utilisateur modales
description: Affichage des interfaces utilisateur modales
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Plug-ins du lecteur Windows Media, affichage des boîtes de dialogue et des messages
- plug-ins, affichage des boîtes de dialogue et des messages
- plug-ins d’interface utilisateur, affichage de boîtes de dialogue et de messages
- Plug-ins d’interface utilisateur, affichage des boîtes de dialogue et des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675885"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="2c76a-107">Affichage des interfaces utilisateur modales</span><span class="sxs-lookup"><span data-stu-id="2c76a-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="2c76a-108">Les plug-ins de l’interface utilisateur ne doivent pas afficher de boîtes de dialogue modales ou de messages en réponse aux appels de méthode du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2c76a-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="2c76a-109">Par exemple, n’affichez pas de boîte de message à partir de votre implémentation de **IWMPPluginUI :: Create**.</span><span class="sxs-lookup"><span data-stu-id="2c76a-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="2c76a-110">Si vous devez afficher une boîte de dialogue ou une boîte de message à partir d’une implémentation de méthode de plug-in d’interface utilisateur qui est appelée par le lecteur, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c76a-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="2c76a-111">Inscrire un nouveau message de fenêtre à l’aide de **RegisterWindowMessage**.</span><span class="sxs-lookup"><span data-stu-id="2c76a-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="2c76a-112">Envoyez le message de fenêtre que vous avez enregistré dans votre fenêtre de plug-in d’interface utilisateur à l’aide de **PostMessage**.</span><span class="sxs-lookup"><span data-stu-id="2c76a-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="2c76a-113">Affichez la boîte de dialogue ou la boîte de message à partir du gestionnaire de messages pour votre nouveau message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2c76a-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c76a-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c76a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c76a-115">**Vue d’ensemble du plug-in d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="2c76a-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




