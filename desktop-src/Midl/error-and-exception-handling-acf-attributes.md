---
title: Attributs ACF de gestion des erreurs et des exceptions
description: Utilisez les attributs suivants pour la gestion des erreurs.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- CCP MIDL, attributs, gestion des erreurs et des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510067"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="695b5-104">Attributs ACF de gestion des erreurs et des exceptions</span><span class="sxs-lookup"><span data-stu-id="695b5-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="695b5-105">Utilisez les attributs suivants pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="695b5-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="695b5-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="695b5-106">Attribute</span></span>                                                                | <span data-ttu-id="695b5-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="695b5-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="695b5-108">État de l’erreur d' [**\_ État de communication**](comm-status.md)[**\_**](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="695b5-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="695b5-109">Laissez votre application cliente gérer les exceptions normalement en provoquant le retour des erreurs de communication et de serveur au client en tant que valeurs de paramètre.</span><span class="sxs-lookup"><span data-stu-id="695b5-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="695b5-110">L’application cliente peut ensuite appeler la fonction runtime RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) pour transmettre un message d’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="695b5-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="695b5-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="695b5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="695b5-112">Importation de fichiers et de bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="695b5-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 