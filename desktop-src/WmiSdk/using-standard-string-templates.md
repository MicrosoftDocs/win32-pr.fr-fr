---
description: Plusieurs consommateurs, tels que le consommateur d’événements active script ou le consommateur d’événements en ligne de commande, ont des propriétés de chaîne avec le qualificateur de modèle.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Utilisation de modèles de chaîne standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866866"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="76894-103">Utilisation de modèles de chaîne standard</span><span class="sxs-lookup"><span data-stu-id="76894-103">Using Standard String Templates</span></span>

<span data-ttu-id="76894-104">Plusieurs consommateurs, tels que le consommateur d’événements active script ou le consommateur d’événements en ligne de commande, ont des propriétés de chaîne avec le qualificateur de **modèle** .</span><span class="sxs-lookup"><span data-stu-id="76894-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="76894-105">Ces propriétés utilisent des modèles de chaîne standard pour construire une chaîne configurée en partie par l’instance de consommateur et en partie par un événement.</span><span class="sxs-lookup"><span data-stu-id="76894-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="76894-106">La structure d’un modèle de chaîne standard est semblable à la spécification de variable d’environnement Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="76894-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="76894-107">La liste suivante présente quelques exemples de la langue du modèle :</span><span class="sxs-lookup"><span data-stu-id="76894-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="76894-108">La chaîne « some Text here » produit toujours la chaîne « some Text here ».</span><span class="sxs-lookup"><span data-stu-id="76894-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="76894-109">« % CPUUtilization% » produit toujours la valeur de la propriété **CPUUtilization** de l’événement qui est remis.</span><span class="sxs-lookup"><span data-stu-id="76894-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="76894-110">Si la propriété n’est pas une chaîne, elle est convertie en chaîne ; par exemple, « 90 » ou « TRUE ».</span><span class="sxs-lookup"><span data-stu-id="76894-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="76894-111">« L’utilisation du processeur de ce processeur est de% CPUUtilization% à ce moment-là » incorpore la valeur de la propriété **CPUUtilization** de l’événement dans la chaîne, ce qui produit un résultat tel que « l’utilisation du processeur de ce processeur est de 90 pour l’instant ».</span><span class="sxs-lookup"><span data-stu-id="76894-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="76894-112">« % TargetInstance. CPUUtilization% » récupère la valeur de la propriété **CPUUtilization** dans l’instance incorporée de la propriété **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="76894-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="76894-113">« %% » produit un seul signe%.</span><span class="sxs-lookup"><span data-stu-id="76894-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="76894-114">Si la propriété Récupérée est un tableau, le tableau entier est généré au format suivant : « (1, 5, 10, 1024) ».</span><span class="sxs-lookup"><span data-stu-id="76894-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="76894-115">S’il n’y a qu’un seul élément dans le tableau, les parenthèses sont omises.</span><span class="sxs-lookup"><span data-stu-id="76894-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="76894-116">S’il n’y a aucun élément dans le tableau, "()" est produit.</span><span class="sxs-lookup"><span data-stu-id="76894-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="76894-117">Si une propriété est un objet incorporé, la représentation MOF de l’objet est générée (semblable à la méthode [**IWbemClassObject :: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).</span><span class="sxs-lookup"><span data-stu-id="76894-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="76894-118">Si une propriété d’un tableau incorporé d’objets est demandée, elle est traitée comme une propriété avec une valeur de tableau.</span><span class="sxs-lookup"><span data-stu-id="76894-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="76894-119">Par exemple :% MyEvents. TargetInstance. DriverLetter% pourrait produire' ("C :", "D :") 'si MyEvents est un tableau d’événements de modification d’instance incorporée.</span><span class="sxs-lookup"><span data-stu-id="76894-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="76894-120">Littéraux de chaîne</span><span class="sxs-lookup"><span data-stu-id="76894-120">String Literals</span></span>

<span data-ttu-id="76894-121">Tout ce qui se trouve à l’intérieur d’une paire de guillemets est considéré comme un littéral de chaîne et ne sera pas remplacé.</span><span class="sxs-lookup"><span data-stu-id="76894-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="76894-122">L’exemple suivant montre la chaîne que le compilateur voit pour « l’utilisation du processeur est% CPUUtilization% ».</span><span class="sxs-lookup"><span data-stu-id="76894-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="76894-123">Cette chaîne produit la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="76894-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="76894-124">En revanche, la chaîne « utilisation de l’UC \\ » est « % CPUUtilization% \\ » est visible par le compilateur comme suit.</span><span class="sxs-lookup"><span data-stu-id="76894-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="76894-125">Cette chaîne produit la sortie suivante, sans substitution de variable.</span><span class="sxs-lookup"><span data-stu-id="76894-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="76894-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76894-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76894-127">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="76894-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



