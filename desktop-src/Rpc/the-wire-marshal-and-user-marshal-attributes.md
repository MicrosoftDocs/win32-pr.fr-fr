---
title: Attributs wire_marshal et user_marshal
description: Cette section décrit l’implémentation de la conversion de type de données de programmeur à l’aide des attributs MIDL \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031654"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="70ba0-103">Attributs du marshaleur \_ de câble et du Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="70ba0-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="70ba0-104">Cette section décrit l’implémentation de la conversion de type de données de programmeur à l’aide des attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) MIDL \] et d' \[ [utilisateur \_ ](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="70ba0-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="70ba0-105">Les informations sont présentées dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="70ba0-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="70ba0-106">Attribut de \_ Marshal de câble</span><span class="sxs-lookup"><span data-stu-id="70ba0-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="70ba0-107">Attribut de \_ Marshal d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="70ba0-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="70ba0-108">La fonction type d' \_ utilisateur</span><span class="sxs-lookup"><span data-stu-id="70ba0-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="70ba0-109">Type \_ UserMarshal (fonction)</span><span class="sxs-lookup"><span data-stu-id="70ba0-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="70ba0-110">Type \_ UserUnmarshal (fonction)</span><span class="sxs-lookup"><span data-stu-id="70ba0-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="70ba0-111">Type \_ UserFree (fonction)</span><span class="sxs-lookup"><span data-stu-id="70ba0-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="70ba0-112">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="70ba0-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 