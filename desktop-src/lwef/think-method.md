---
title: Méthode de réflexion
description: Méthode de réflexion
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842198"
---
# <a name="think-method"></a><span data-ttu-id="02f87-103">Méthode de réflexion</span><span class="sxs-lookup"><span data-stu-id="02f87-103">Think Method</span></span>

<span data-ttu-id="02f87-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02f87-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="02f87-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="02f87-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="02f87-106">Affiche le texte spécifié pour le caractère spécifié dans une bulle de mot « pensée ».</span><span class="sxs-lookup"><span data-stu-id="02f87-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="02f87-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="02f87-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="02f87-108">\*agent ***. Caractères («*** CharacterID \* \* * »).* \*  \[ *Texte* de réflexion\]</span><span class="sxs-lookup"><span data-stu-id="02f87-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="02f87-109">Partie</span><span class="sxs-lookup"><span data-stu-id="02f87-109">Part</span></span>   | <span data-ttu-id="02f87-110">Description</span><span class="sxs-lookup"><span data-stu-id="02f87-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="02f87-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="02f87-111">*Text*</span></span> | <span data-ttu-id="02f87-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="02f87-112">Optional.</span></span> <span data-ttu-id="02f87-113">Chaîne qui spécifie le résultat de la réflexion du caractère.</span><span class="sxs-lookup"><span data-stu-id="02f87-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02f87-114">Notes</span><span class="sxs-lookup"><span data-stu-id="02f87-114">Remarks</span></span>

<span data-ttu-id="02f87-115">À l’instar de la méthode [**Speak**](speak-method.md) , la méthode **Song** est une demande en file d’attente qui affiche du texte dans une bulle de mot, sauf que la bulle de **pense** -bulle est différente visuellement.</span><span class="sxs-lookup"><span data-stu-id="02f87-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="02f87-116">En outre, la bulle prend uniquement en charge la balise de contrôle de voix de signets (**\\ MRK**) et ignore toutes les autres balises de contrôle vocal.</span><span class="sxs-lookup"><span data-stu-id="02f87-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="02f87-117">Contrairement à **Speak**, la méthode de **réflexion** ne modifie pas l’état d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="02f87-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="02f87-118">Les propriétés de l’objet [**Balloon**](/windows/desktop/lwef/the-balloon-object) affectent la sortie des méthodes [**Speak**](speak-method.md) et **Song** .</span><span class="sxs-lookup"><span data-stu-id="02f87-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="02f87-119">Par exemple, la propriété [**Enabled**](enabled-property.md) de l’objet **Balloon** doit avoir la **valeur true** pour que le texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="02f87-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="02f87-120">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="02f87-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="02f87-121">En outre, si le fichier n’a pas été chargé, le serveur définit la propriété [**Status**](status-property.md) de l’objet de **requête** sur « failed » avec un numéro de code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="02f87-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="02f87-122">La césure automatique des mots de l’agent dans le mot-bulle arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace ou tabulation).</span><span class="sxs-lookup"><span data-stu-id="02f87-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="02f87-123">Toutefois, si ce n’est pas le cas, il peut endommager un mot pour l’ajuster à la bulle.</span><span class="sxs-lookup"><span data-stu-id="02f87-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="02f87-124">Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un caractère d’espace de largeur nulle Unicode (0x200B) entre les caractères pour définir des césures lexicales.</span><span class="sxs-lookup"><span data-stu-id="02f87-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="02f87-125">Définissez l’ID de langue du caractère avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="02f87-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 