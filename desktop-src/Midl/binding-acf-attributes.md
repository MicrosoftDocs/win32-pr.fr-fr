---
title: Liaison d’attributs ACF
description: Spécifiez la façon dont le client se connecte au serveur pour les appels de procédure distante avec les attributs énumérés dans le tableau suivant.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL, attributs, liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029608"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="22080-104">Liaison d’attributs ACF</span><span class="sxs-lookup"><span data-stu-id="22080-104">Binding ACF Attributes</span></span>

<span data-ttu-id="22080-105">Spécifiez la façon dont le client se connecte au serveur pour les appels de procédure distante avec les attributs énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22080-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="22080-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="22080-106">Attribute</span></span>                                                          | <span data-ttu-id="22080-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="22080-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22080-108">**async**</span><span class="sxs-lookup"><span data-stu-id="22080-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="22080-109">Définit un handle qui permet à l’appelant de passer un appel asynchrone et de retourner immédiatement sans attendre les résultats, puis de se resynchroniser avec la fonction appelée pour recevoir des données une fois l’appel terminé.</span><span class="sxs-lookup"><span data-stu-id="22080-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="22080-110">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="22080-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="22080-111">Indique à MIDL de laisser le code stub contrôler automatiquement la liaison.</span><span class="sxs-lookup"><span data-stu-id="22080-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="22080-112">Il s’agit de la valeur par défaut si vous ne spécifiez pas de handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="22080-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="22080-113">**handle de contexte \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="22080-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="22080-114">Garantit qu’un handle de contexte ne sera jamais sérialisé, quel que soit le comportement par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="22080-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="22080-115">**\_sérialisation du handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="22080-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="22080-116">Garantit qu’un handle de contexte sera toujours sérialisé, quel que soit le comportement par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="22080-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="22080-117">**\_handle explicite**</span><span class="sxs-lookup"><span data-stu-id="22080-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="22080-118">Permet à l’application cliente de contrôler la liaison avec un paramètre explicite dans chaque procédure.</span><span class="sxs-lookup"><span data-stu-id="22080-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="22080-119">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="22080-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="22080-120">Spécifie un handle pour les procédures qui n’ont pas de paramètre de handle explicite.</span><span class="sxs-lookup"><span data-stu-id="22080-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="22080-121">L’application cliente contrôle toujours la liaison.</span><span class="sxs-lookup"><span data-stu-id="22080-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="22080-122">**\_handle de contexte strict \_**</span><span class="sxs-lookup"><span data-stu-id="22080-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="22080-123">Garantit que les méthodes de l’interface n’acceptent que des handles de contexte qui ont été créés par une méthode de cette interface.</span><span class="sxs-lookup"><span data-stu-id="22080-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 




