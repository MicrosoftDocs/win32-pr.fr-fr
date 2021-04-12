---
description: Les caractères définis par l’utilisateur final (EUDC) dans les jeux de caractères codés sur deux octets (DBCS) et les caractères de zone d’utilisation privée (PUA) en Unicode sont des caractères personnalisés.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caractères de zone d’utilisation privée et définis par l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320233"
---
# <a name="end-user-defined-and-private-use-area-characters"></a><span data-ttu-id="24d77-103">Caractères de zone d’utilisation privée et définis par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="24d77-103">End-User-Defined and Private Use Area Characters</span></span>

<span data-ttu-id="24d77-104">Les caractères définis par l’utilisateur final (EUDC) dans les [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS) et les caractères de zone d’utilisation privée (PUA) en [Unicode](unicode.md) sont des caractères personnalisés.</span><span class="sxs-lookup"><span data-stu-id="24d77-104">End-user-defined characters (EUDC) in [double-byte character sets](double-byte-character-sets.md) (DBCSs) and private use area (PUA) characters in [Unicode](unicode.md) are custom characters.</span></span> <span data-ttu-id="24d77-105">Elles peuvent être définies et implémentées par un utilisateur final ou par une autre partie, telle qu’un fabricant d’équipements, un groupe d’utilisateurs, un organisme gouvernemental ou une société de conception de polices.</span><span class="sxs-lookup"><span data-stu-id="24d77-105">They can be defined and implemented either by an end user or by another party, such as an equipment manufacturer, a user group, a government body, or a font design company.</span></span> <span data-ttu-id="24d77-106">Leur utilisation permet aux utilisateurs de former des noms et d’autres mots à l’aide de caractères qui ne sont pas disponibles dans les polices d’écran et d’imprimante standard.</span><span class="sxs-lookup"><span data-stu-id="24d77-106">Their use enables users to form names and other words using characters that are not available in standard screen and printer fonts.</span></span>

<span data-ttu-id="24d77-107">Les caractères EUDC et PUA peuvent être attribués différemment ou non attribués sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="24d77-107">The EUDC and PUA characters can be assigned differently, or not assigned at all, on different computers.</span></span> <span data-ttu-id="24d77-108">Certaines pages de codes ont des extensions qui réutilisent la plage EUDC, et ces extensions peuvent entrer en conflit.</span><span class="sxs-lookup"><span data-stu-id="24d77-108">Some code pages have extensions that reuse the EUDC range, and these extensions can conflict with each other.</span></span> <span data-ttu-id="24d77-109">Dans d’autres cas, un fabricant peut fournir un ensemble personnalisé de caractères dans l’une de ces plages.</span><span class="sxs-lookup"><span data-stu-id="24d77-109">In other cases, a manufacturer might provide a custom set of characters in one of these ranges.</span></span> <span data-ttu-id="24d77-110">En outre, les groupes d’utilisateurs peuvent tenter de fournir des caractères supplémentaires dans le PUA.</span><span class="sxs-lookup"><span data-stu-id="24d77-110">Additionally, user groups can attempt to provide additional characters in the PUA.</span></span> <span data-ttu-id="24d77-111">Différentes combinaisons de ces cas peuvent entraîner un conflit.</span><span class="sxs-lookup"><span data-stu-id="24d77-111">Different combinations of these cases can cause conflict.</span></span> <span data-ttu-id="24d77-112">Lorsque vous créez des applications qui reposent sur des caractères EUDC ou PUA, vous devez garder à l’esprit les interprétations conflictuelles d’un point de code individuel.</span><span class="sxs-lookup"><span data-stu-id="24d77-112">When creating applications that rely on EUDC or PUA characters, you should keep in mind the conflicting interpretations of an individual code point.</span></span>

<span data-ttu-id="24d77-113">Les rubriques suivantes décrivent les polices qui prennent en charge EUDCs, ainsi que l’accès et la gestion de ces caractères :</span><span class="sxs-lookup"><span data-stu-id="24d77-113">The following topics discuss the fonts that support EUDCs, and access and management for these characters:</span></span>

-   [<span data-ttu-id="24d77-114">Jeux de caractères et polices</span><span class="sxs-lookup"><span data-stu-id="24d77-114">Character Sets and Fonts</span></span>](character-sets-and-fonts.md)
-   [<span data-ttu-id="24d77-115">Entrées de Registre EUDC</span><span class="sxs-lookup"><span data-stu-id="24d77-115">EUDC Registry Entries</span></span>](eudc-registry-entries.md)

## <a name="related-topics"></a><span data-ttu-id="24d77-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24d77-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24d77-117">À propos d’Unicode et des jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="24d77-117">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



