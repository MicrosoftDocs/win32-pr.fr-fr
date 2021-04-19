---
description: Le type de données GUID est une chaîne de texte représentant un identificateur de classe (ID). COM doit être en mesure de convertir la chaîne en un ID de classe valide. Tous les GUID doivent être créés en majuscules.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541843"
---
# <a name="guid"></a><span data-ttu-id="e71f0-105">GUID</span><span class="sxs-lookup"><span data-stu-id="e71f0-105">GUID</span></span>

<span data-ttu-id="e71f0-106">Le type de données GUID est une chaîne de texte représentant un identificateur de classe (ID).</span><span class="sxs-lookup"><span data-stu-id="e71f0-106">The GUID data type is a text string representing a Class identifier (ID).</span></span> <span data-ttu-id="e71f0-107">COM doit être en mesure de convertir la chaîne en un ID de classe valide.</span><span class="sxs-lookup"><span data-stu-id="e71f0-107">COM must be able to convert the string to a valid Class ID.</span></span> <span data-ttu-id="e71f0-108">Tous les GUID doivent être créés en majuscules.</span><span class="sxs-lookup"><span data-stu-id="e71f0-108">All GUIDs must be authored in uppercase.</span></span>

<span data-ttu-id="e71f0-109">Le format valide pour un GUID est {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, où X est un chiffre hexadécimal (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F).</span><span class="sxs-lookup"><span data-stu-id="e71f0-109">The valid format for a GUID is {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} where X is a hex digit (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).</span></span>

<span data-ttu-id="e71f0-110">Notez que les utilitaires tels que GUIDGEN peuvent générer des GUID contenant des lettres minuscules.</span><span class="sxs-lookup"><span data-stu-id="e71f0-110">Note that utilities such as GUIDGEN can generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="e71f0-111">Ils doivent tous être remplacés par des lettres majuscules avant que le programme d’installation ne puisse utiliser le GUID comme code de produit, code de package ou code de composant valide.</span><span class="sxs-lookup"><span data-stu-id="e71f0-111">These must all be changed to uppercase letters before the GUID can be used by the installer as a valid product code, package code, or component code.</span></span>

 

 



