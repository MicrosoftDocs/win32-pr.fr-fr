---
title: Handles de liaison
description: La liaison est le processus de création d’une connexion logique entre un programme client et un programme serveur. Les informations qui composent la liaison entre le client et le serveur sont représentées par une structure appelée descripteur de liaison.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507954"
---
# <a name="binding-handles"></a><span data-ttu-id="d278a-104">Handles de liaison</span><span class="sxs-lookup"><span data-stu-id="d278a-104">Binding Handles</span></span>

<span data-ttu-id="d278a-105">La liaison est le processus de création d’une connexion logique entre un programme client et un programme serveur.</span><span class="sxs-lookup"><span data-stu-id="d278a-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="d278a-106">Les informations qui composent la liaison entre le client et le serveur sont représentées par une structure appelée descripteur de liaison.</span><span class="sxs-lookup"><span data-stu-id="d278a-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="d278a-107">Un handle de liaison est analogue à un descripteur de fichier retourné par la fonction de la bibliothèque Runtime C fopen, ou un handle de fenêtre retourné par la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="d278a-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="d278a-108">Comme avec ces handles, votre application ne peut pas accéder directement aux informations contenues dans le handle de liaison et les manipuler.</span><span class="sxs-lookup"><span data-stu-id="d278a-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="d278a-109">Les informations contenues dans une structure de données de handle de liaison sont uniquement disponibles pour les bibliothèques Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="d278a-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="d278a-110">Vous fournissez le descripteur, les bibliothèques Runtime accèdent aux données appropriées et les manipulent.</span><span class="sxs-lookup"><span data-stu-id="d278a-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="d278a-111">Cette section présente une discussion sur les descripteurs de liaison dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d278a-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="d278a-112">Types de handles de liaison</span><span class="sxs-lookup"><span data-stu-id="d278a-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="d278a-113">Liaison côté client</span><span class="sxs-lookup"><span data-stu-id="d278a-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="d278a-114">Liaison côté serveur</span><span class="sxs-lookup"><span data-stu-id="d278a-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="d278a-115">Handles entièrement et partiellement liés</span><span class="sxs-lookup"><span data-stu-id="d278a-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="d278a-116">Interprétation des informations de liaison</span><span class="sxs-lookup"><span data-stu-id="d278a-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="d278a-117">Extensions de Binding-Handle Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="d278a-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="d278a-118">Fonctions de gestion de liaison</span><span class="sxs-lookup"><span data-stu-id="d278a-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="d278a-119">La base de données du service de noms RPC</span><span class="sxs-lookup"><span data-stu-id="d278a-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 