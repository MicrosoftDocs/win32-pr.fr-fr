---
title: Propriété FontCharSet
description: Propriété FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311017"
---
# <a name="fontcharset-property"></a><span data-ttu-id="4e3a2-103">Propriété FontCharSet</span><span class="sxs-lookup"><span data-stu-id="4e3a2-103">FontCharSet Property</span></span>

<span data-ttu-id="4e3a2-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e3a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4e3a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="4e3a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4e3a2-106">Retourne ou définit le jeu de caractères pour la police affichée dans la bulle de texte du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="4e3a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="4e3a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4e3a2-108">\*agent ***. Caractères («*** CharacterID \* \* * »). Valeur Balloon. FontCharSet* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="4e3a2-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="4e3a2-109">Partie</span><span class="sxs-lookup"><span data-stu-id="4e3a2-109">Part</span></span>    | <span data-ttu-id="4e3a2-110">Description</span><span class="sxs-lookup"><span data-stu-id="4e3a2-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3a2-111">*value*</span><span class="sxs-lookup"><span data-stu-id="4e3a2-111">*value*</span></span> | <span data-ttu-id="4e3a2-112">Valeur entière qui spécifie le jeu de caractères utilisé par la police.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="4e3a2-113">Voici quelques paramètres courants pour la valeur : 0 caractères Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4e3a2-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="4e3a2-114">1 jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-114">1 Default character set.</span></span><br/> <span data-ttu-id="4e3a2-115">2 le jeu de caractères de symbole.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="4e3a2-116">128 jeu de caractères codés sur deux octets (DBCS) propre à la version japonaise de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="4e3a2-117">129 jeu de caractères codés sur deux octets (DBCS) propre à la version coréenne de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="4e3a2-118">134 jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois simplifié.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="4e3a2-119">136 jeu de caractères codés sur deux octets (DBCS) propre à la version en chinois traditionnel de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="4e3a2-120">255 caractères étendus normalement affichés par les applications Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="4e3a2-121">Pour les autres valeurs de jeu de caractères, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e3a2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4e3a2-122">Remarks</span></span>

<span data-ttu-id="4e3a2-123">La valeur par défaut du jeu de caractères de la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4e3a2-124">En outre, l’utilisateur peut remplacer les paramètres de jeu de caractères pour tous les caractères de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="4e3a2-125">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="4e3a2-126">Si vous utilisez un caractère que vous n’avez pas compilé, vérifiez les propriétés [**FontName**](fontname-property.md) et **FontCharSet** pour déterminer s’ils sont appropriés pour vos paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="4e3a2-127">Vous devrez peut-être définir ces valeurs avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="4e3a2-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4e3a2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e3a2-128">See Also</span></span>

[<span data-ttu-id="4e3a2-129">**FontName, propriété**</span><span class="sxs-lookup"><span data-stu-id="4e3a2-129">**FontName property**</span></span>](fontname-property.md)


 

 





