---
description: Préfixez toujours un fichier texte brut Unicode avec une marque d’ordre d’octet, qui informe une application recevant le fichier que le fichier est classé en octets.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Utilisation des marques d’ordre des octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529481"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="f1fb4-103">Utilisation des marques d’ordre des octets</span><span class="sxs-lookup"><span data-stu-id="f1fb4-103">Using Byte Order Marks</span></span>

<span data-ttu-id="f1fb4-104">Préfixez toujours un fichier texte brut Unicode avec une marque d’ordre d’octet, qui informe une application recevant le fichier que le fichier est classé en octets.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="f1fb4-105">Les marques d’ordre d’octet disponibles sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="f1fb4-106">Étant donné que le texte brut Unicode est une séquence de valeurs de code de 16 bits, il est sensible à l’ordre des octets utilisé lorsque le texte est écrit.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="f1fb4-107">Une marque d’ordre d’octet n’est pas un caractère de contrôle qui sélectionne l’ordre d’octet du texte.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="f1fb4-108">Marque d'ordre d'octet</span><span class="sxs-lookup"><span data-stu-id="f1fb4-108">Byte order mark</span></span> | <span data-ttu-id="f1fb4-109">Description</span><span class="sxs-lookup"><span data-stu-id="f1fb4-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="f1fb4-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="f1fb4-110">EF BB BF</span></span>        | <span data-ttu-id="f1fb4-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="f1fb4-111">UTF-8</span></span>                 |
| <span data-ttu-id="f1fb4-112">FF FE</span><span class="sxs-lookup"><span data-stu-id="f1fb4-112">FF FE</span></span>           | <span data-ttu-id="f1fb4-113">UTF-16, Little endian</span><span class="sxs-lookup"><span data-stu-id="f1fb4-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="f1fb4-114">FE FF</span><span class="sxs-lookup"><span data-stu-id="f1fb4-114">FE FF</span></span>           | <span data-ttu-id="f1fb4-115">UTF-16, Big endian</span><span class="sxs-lookup"><span data-stu-id="f1fb4-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="f1fb4-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="f1fb4-116">FF FE 00 00</span></span>     | <span data-ttu-id="f1fb4-117">UTF-32, Little endian</span><span class="sxs-lookup"><span data-stu-id="f1fb4-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="f1fb4-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="f1fb4-118">00 00 FE FF</span></span>     | <span data-ttu-id="f1fb4-119">UTF-32, Big-endian</span><span class="sxs-lookup"><span data-stu-id="f1fb4-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="f1fb4-120">Microsoft utilise UTF-16, primauté des octets de poids faible.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="f1fb4-121">Dans l’idéal, tout le texte Unicode suit un seul jeu de règles de classement des octets.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="f1fb4-122">Toutefois, cela n’est pas possible car les microprocesseurs diffèrent au niveau de l’emplacement de l’octet le moins significatif.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="f1fb4-123">Les processeurs Intel et MIPS déplacent d’abord l’octet le moins significatif, tandis que les processeurs Motorola (et tous les fichiers Unicode inversé en octets) le déplacent en dernier.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="f1fb4-124">Avec un seul ensemble de règles de classement des octets, les utilisateurs d’un type de microprocesseur sont obligés de permuter l’ordre des octets chaque fois qu’un fichier texte brut est lu ou écrit, même si le fichier n’est jamais transféré vers un autre système d’exploitation basé sur un microprocesseur différent.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="f1fb4-125">L’emplacement par défaut pour spécifier l’ordre des octets est dans un en-tête de fichier, mais les fichiers texte n’ont pas d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="f1fb4-126">Par conséquent, Unicode a défini un caractère (U + FEFF) et un caractère non-caractère (U + FFFE) comme marques d’ordre d’octet.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="f1fb4-127">Il s’agit d’images en miroir les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="f1fb4-128">Étant donné que la séquence U + FEFF est extrêmement rare au début d’un fichier texte non-Unicode normal, elle peut servir de marqueur ou de signature implicite pour identifier le fichier en tant que fichier Unicode.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="f1fb4-129">Les applications qui lisent à la fois les fichiers texte Unicode et non-Unicode doivent utiliser la présence de cette séquence comme un indicateur qui indique que le fichier est probablement un fichier Unicode.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="f1fb4-130">Comparez cette technique à l’utilisation du marqueur EOF MS-DOS pour mettre fin aux fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="f1fb4-131">Quand une application trouve U + FEFF au début d’un fichier texte, elle traite généralement le fichier en tant que fichier Unicode, bien qu’elle puisse effectuer d’autres vérifications heuristiques pour la vérification.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="f1fb4-132">Une telle vérification peut être aussi simple que le test pour déterminer si la variation des octets de poids faible est beaucoup plus élevée que la variation dans les octets de poids fort.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="f1fb4-133">Par exemple, si le texte ASCII est converti en texte Unicode, chaque seconde octet est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="f1fb4-134">En outre, la vérification des caractères de saut de ligne et de retour chariot (U + 000A et U + 000D) et de la taille du fichier pair ou impair peut fournir un indicateur fort de la nature du fichier.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="f1fb4-135">Quand une application trouve U + FFFE au début d’un fichier texte, elle l’interprète pour signifier que le fichier est un fichier Unicode inversé par octet.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="f1fb4-136">L’application peut échanger l’ordre des octets ou alerter l’utilisateur qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="f1fb4-137">Étant donné que le caractère de marque d’ordre d’octet Unicode est introuvable dans une page de codes, il disparaît si les données sont converties en ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="f1fb4-138">Contrairement à d’autres caractères Unicode, il n’est pas remplacé par un caractère par défaut lorsqu’il est converti.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="f1fb4-139">Si une marque d’ordre d’octet se trouve au milieu d’un fichier, elle n’est pas interprétée comme un caractère Unicode et n’a aucun effet sur la sortie de texte.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="f1fb4-140">La valeur Unicode U + FFFF est illégale dans les fichiers texte bruts et ne peut pas être transmise entre les applications.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="f1fb4-141">Elle est réservée à l’utilisation privée d’une application.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f1fb4-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1fb4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1fb4-143">Utilisation de caractères spéciaux en Unicode</span><span class="sxs-lookup"><span data-stu-id="f1fb4-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



