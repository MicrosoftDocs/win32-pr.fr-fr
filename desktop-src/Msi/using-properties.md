---
description: Les sections suivantes décrivent l’utilisation des propriétés de programme d’installation intégrées et des propriétés supplémentaires définies par l’auteur du package.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilisation de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113243"
---
# <a name="using-properties"></a><span data-ttu-id="2c921-103">Utilisation de propriétés</span><span class="sxs-lookup"><span data-stu-id="2c921-103">Using Properties</span></span>

<span data-ttu-id="2c921-104">Les sections suivantes décrivent l’utilisation des propriétés de programme d’installation intégrées et des propriétés supplémentaires définies par l’auteur du package.</span><span class="sxs-lookup"><span data-stu-id="2c921-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="2c921-105">Les propriétés peuvent être des propriétés [publiques](public-properties.md) ou [privées](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2c921-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="2c921-106">Chaque propriété qui doit être définie lors de l’initialisation du programme d’installation doit avoir son nom et sa valeur initiale listés dans la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="2c921-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="2c921-107">Les propriétés ayant une valeur NULL ne sont pas répertoriées dans la table des propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c921-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="2c921-108">Vous pouvez récupérer ou définir des propriétés à partir de programmes et d’actions personnalisées et définir des propriétés publiques à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2c921-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="2c921-109">Le processus d’installation peut être modifié à l’aide de propriétés dans des instructions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="2c921-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="2c921-110">Restrictions sur les noms de propriété</span><span class="sxs-lookup"><span data-stu-id="2c921-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="2c921-111">Initialisation des valeurs de propriété</span><span class="sxs-lookup"><span data-stu-id="2c921-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="2c921-112">Obtention et définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="2c921-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="2c921-113">Utilisation des propriétés dans les instructions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="2c921-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="2c921-114">Utilisation d’une propriété de répertoire dans un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c921-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="2c921-115">N’utilisez pas de propriétés pour les mots de passe ou d’autres informations qui doivent rester sécurisées.</span><span class="sxs-lookup"><span data-stu-id="2c921-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="2c921-116">Le programme d’installation peut écrire la valeur d’une propriété créée dans la table de propriétés ou créée au moment de l’exécution dans un journal ou dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="2c921-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2c921-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c921-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c921-118">À propos des propriétés</span><span class="sxs-lookup"><span data-stu-id="2c921-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="2c921-119">Référence de propriété</span><span class="sxs-lookup"><span data-stu-id="2c921-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



