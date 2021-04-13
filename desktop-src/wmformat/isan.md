---
title: ISAN
description: L’attribut ISAN contient le numéro audiovisuel standard international qui identifie le contenu.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Format Windows Media ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381603"
---
# <a name="isan"></a><span data-ttu-id="88aff-104">ISAN</span><span class="sxs-lookup"><span data-stu-id="88aff-104">ISAN</span></span>

<span data-ttu-id="88aff-105">L’attribut **ISAN** contient le numéro audiovisuel standard international qui identifie le contenu.</span><span class="sxs-lookup"><span data-stu-id="88aff-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="88aff-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="88aff-106">Global Constant</span></span>

<span data-ttu-id="88aff-107">\_wszISAN g</span><span class="sxs-lookup"><span data-stu-id="88aff-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="88aff-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="88aff-108">Data Type</span></span>

<span data-ttu-id="88aff-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="88aff-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="88aff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="88aff-110">Remarks</span></span>

<span data-ttu-id="88aff-111">ISAN est une norme internationale pour identifier les travaux audiovisuels.</span><span class="sxs-lookup"><span data-stu-id="88aff-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="88aff-112">Pour plus d’informations sur ISAN, visitez le [site Web](https://www.isan.org/)standard.</span><span class="sxs-lookup"><span data-stu-id="88aff-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="88aff-113">L’objet de l’éditeur de métadonnées vérifie la chaîne ISAN lorsque vous définissez cet attribut.</span><span class="sxs-lookup"><span data-stu-id="88aff-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="88aff-114">La mise en forme de chaîne acceptable, comme décrit dans la section 4,1 de la spécification ISAN, se compose de 16 chiffres hexadécimaux, éventuellement séparés par des espaces blancs ou des traits d’Union en segments de 4 chiffres.</span><span class="sxs-lookup"><span data-stu-id="88aff-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="88aff-115">Le nombre mis en forme doit être suivi, également éventuellement séparé par un espace ou un trait d’Union, par un caractère de vérification valide.</span><span class="sxs-lookup"><span data-stu-id="88aff-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="88aff-116">Le caractère de vérification peut être un chiffre décimal ou une lettre majuscule.</span><span class="sxs-lookup"><span data-stu-id="88aff-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="88aff-117">Pour plus d’informations sur la façon de dériver le numéro de chèque, reportez-vous à l’annexe A du Guide de l’utilisateur ISAN.</span><span class="sxs-lookup"><span data-stu-id="88aff-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="88aff-118">La chaîne ISAN standard peut être suivie d’informations sur la version.</span><span class="sxs-lookup"><span data-stu-id="88aff-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="88aff-119">Le cas échéant, les informations de version se composent de huit chiffres hexadécimaux suivis d’un numéro de chèque.</span><span class="sxs-lookup"><span data-stu-id="88aff-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="88aff-120">La mise en forme de ces caractères suit les mêmes règles que la chaîne de base.</span><span class="sxs-lookup"><span data-stu-id="88aff-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="88aff-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="88aff-121">Examples</span></span>

<span data-ttu-id="88aff-122">Voici trois chaînes mises en forme de façon acceptable pour un exemple de ISAN.</span><span class="sxs-lookup"><span data-stu-id="88aff-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="88aff-123">La chaîne suivante montre le format d’un ISAN avec les informations de version.</span><span class="sxs-lookup"><span data-stu-id="88aff-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="88aff-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88aff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88aff-125">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="88aff-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




