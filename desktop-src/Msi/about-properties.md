---
description: Windows Installer pouvez configurer l’installation de logiciels à l’aide des valeurs des variables définies dans un package d’installation ou par l’utilisateur.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: À propos des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202572"
---
# <a name="about-properties"></a><span data-ttu-id="0dbd6-103">À propos des propriétés</span><span class="sxs-lookup"><span data-stu-id="0dbd6-103">About Properties</span></span>

<span data-ttu-id="0dbd6-104">Windows Installer pouvez configurer l’installation de logiciels à l’aide des valeurs des variables définies dans un package d’installation ou par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0dbd6-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="0dbd6-105">Windows Installer utilise trois catégories de variables globales au cours d’une installation :</span><span class="sxs-lookup"><span data-stu-id="0dbd6-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="0dbd6-106">Propriétés privées : le programme d’installation utilise des propriétés privées en interne et leurs valeurs doivent être créées dans la base de données d’installation ou définies sur des valeurs déterminées par l’environnement d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0dbd6-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="0dbd6-107">Propriétés publiques : les propriétés publiques peuvent être créées dans la base de données et modifiées par un utilisateur ou un administrateur système sur la ligne de commande, en appliquant une transformation ou en interagissant avec une interface utilisateur créée.</span><span class="sxs-lookup"><span data-stu-id="0dbd6-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="0dbd6-108">Propriétés publiques restreintes : pour des raisons de sécurité, l’auteur d’un package d’installation peut restreindre les propriétés publiques qu’un utilisateur peut modifier.</span><span class="sxs-lookup"><span data-stu-id="0dbd6-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="0dbd6-109">Toutes les propriétés ne doivent pas être définies dans chaque package, il existe un petit ensemble de propriétés requises qui doivent être définies dans chaque package.</span><span class="sxs-lookup"><span data-stu-id="0dbd6-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="0dbd6-110">Le programme d’installation définit les valeurs des propriétés dans un ordre de priorité particulier.</span><span class="sxs-lookup"><span data-stu-id="0dbd6-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="0dbd6-111">Propriétés privées</span><span class="sxs-lookup"><span data-stu-id="0dbd6-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="0dbd6-112">Propri&amp;#233;t&amp;#233;s publiques</span><span class="sxs-lookup"><span data-stu-id="0dbd6-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="0dbd6-113">Propriétés publiques restreintes</span><span class="sxs-lookup"><span data-stu-id="0dbd6-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="0dbd6-114">Propriétés requises</span><span class="sxs-lookup"><span data-stu-id="0dbd6-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="0dbd6-115">Ordre de priorité des propriétés</span><span class="sxs-lookup"><span data-stu-id="0dbd6-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="0dbd6-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0dbd6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dbd6-117">Utilisation de propriétés</span><span class="sxs-lookup"><span data-stu-id="0dbd6-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="0dbd6-118">Référence de propriété</span><span class="sxs-lookup"><span data-stu-id="0dbd6-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



