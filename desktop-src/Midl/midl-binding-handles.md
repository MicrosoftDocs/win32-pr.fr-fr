---
title: Handles de liaison MIDL
description: Les handles de liaison sont des objets de données qui représentent la liaison entre le client et le serveur.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- types de données MIDL, handles de liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031072"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="e23b6-104">Handles de liaison MIDL</span><span class="sxs-lookup"><span data-stu-id="e23b6-104">MIDL Binding Handles</span></span>

<span data-ttu-id="e23b6-105">Les handles de liaison sont des objets de données qui représentent la liaison entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="e23b6-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="e23b6-106">MIDL prend en charge le [**handle \_**](handle-t.md)de type de base t.</span><span class="sxs-lookup"><span data-stu-id="e23b6-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="e23b6-107">Les handles de ce type sont appelés « Handles primitifs ».</span><span class="sxs-lookup"><span data-stu-id="e23b6-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="e23b6-108">Vous pouvez définir vos propres types de handles à l’aide de l’attribut **\[ descripteur \]** .</span><span class="sxs-lookup"><span data-stu-id="e23b6-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="e23b6-109">Les handles définis de cette façon sont appelés Handles « définis par l’utilisateur » ou « personnalisés » ou « génériques ».</span><span class="sxs-lookup"><span data-stu-id="e23b6-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="e23b6-110">Vous pouvez également définir un handle qui gère les informations d’État à l’aide de l’attribut de **\[** [**\_ handle de contexte**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e23b6-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="e23b6-111">Les handles définis de cette façon sont appelés Handles « Context ».</span><span class="sxs-lookup"><span data-stu-id="e23b6-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="e23b6-112">Si aucune information d’État n’est nécessaire et que vous ne choisissez pas d’appeler les bibliothèques Runtime RPC pour gérer le handle, vous pouvez demander que les bibliothèques Runtime fournissent une liaison automatique.</span><span class="sxs-lookup"><span data-stu-id="e23b6-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="e23b6-113">Pour ce faire, utilisez le **\[** [**\_ descripteur automatique**](auto-handle.md)de mot clé ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="e23b6-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="e23b6-114">Vous pouvez spécifier une variable globale comme handle de liaison à l’aide du mot clé ACF **\[** [**\_ handle implicite**](implicit-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e23b6-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="e23b6-115">Le mot clé **\[ \_ handle \] explicite** est utilisé pour indiquer que chaque fonction distante a un handle explicitement spécifié.</span><span class="sxs-lookup"><span data-stu-id="e23b6-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="e23b6-116">Pour plus d’informations, consultez [liaison et Handles](/windows/desktop/Rpc/binding-and-handles).</span><span class="sxs-lookup"><span data-stu-id="e23b6-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 