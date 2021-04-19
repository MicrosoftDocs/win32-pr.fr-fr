---
description: La couche données contient souvent des informations principalement statiques&\# 8212 ; les informations sont conservées sur un support durable.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimiser les appels entre la logique métier COM+ et les données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516780"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="39d6a-103">Optimisation des interactions entre le niveau de logique métier COM+ et la couche données</span><span class="sxs-lookup"><span data-stu-id="39d6a-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="39d6a-104">La couche données contient souvent des informations essentiellement statiques : les informations sont conservées sur un support durable.</span><span class="sxs-lookup"><span data-stu-id="39d6a-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="39d6a-105">Étant donné que ce niveau englobe des informations qui sont principalement statiques, il est nécessaire d’analyser minutieusement les goulots d’étranglement potentiels.</span><span class="sxs-lookup"><span data-stu-id="39d6a-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="39d6a-106">Outre la possibilité évidente de goulots d’étranglement de connexion, les zones réactives peuvent être dues à des enregistrements fréquemment sollicités, à des méthodes d’accès aux données inefficaces et à la nécessité de coordonner l’accès aux systèmes hérités.</span><span class="sxs-lookup"><span data-stu-id="39d6a-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="39d6a-107">Connexion à la couche données</span><span class="sxs-lookup"><span data-stu-id="39d6a-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="39d6a-108">Deux considérations jouent un rôle important dans la conception d’une couche données pour une application COM+ : le regroupement de connexions et l’activation de la [fonction juste-à-temps (JIT) com+](com--just-in-time-activation.md), ainsi que l’utilisation de DSN.</span><span class="sxs-lookup"><span data-stu-id="39d6a-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="39d6a-109">Les composants qui établissent des connexions à la couche données doivent utiliser le [regroupement d’objets com+](com--object-pooling.md) défini sur le composant.</span><span class="sxs-lookup"><span data-stu-id="39d6a-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="39d6a-110">Lors de la création de DSN, utilisez les chaînes de constructeur d’objet spécifiées sur le composant au lieu de créer un DSN de fichier.</span><span class="sxs-lookup"><span data-stu-id="39d6a-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="39d6a-111">Les noms de sources de fichier sont plus lents qu’une connexion utilisant une chaîne de constructeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="39d6a-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="39d6a-112">Les chaînes du constructeur d’objet peuvent être spécifiées dans la feuille de propriétés du composant.</span><span class="sxs-lookup"><span data-stu-id="39d6a-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="39d6a-113">Pour plus d’informations, consultez [chaînes de constructeur d’objet com+](com--object-constructor-strings.md).</span><span class="sxs-lookup"><span data-stu-id="39d6a-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="39d6a-114">Si vous utilisez des composants pour accéder à une base de données SQL Server, utilisez le regroupement d’objets COM+ au lieu du regroupement de connexions SQL.</span><span class="sxs-lookup"><span data-stu-id="39d6a-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="39d6a-115">Si votre composant utilise ADO pour extraire plusieurs recordsets, établissez plusieurs connexions pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="39d6a-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="39d6a-116">Lorsque ADO Récupère plusieurs recordsets, il crée plusieurs connexions en arrière-plan si vous ne les créez pas.</span><span class="sxs-lookup"><span data-stu-id="39d6a-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="39d6a-117">Si vous les créez, vous pouvez les regrouper et avoir davantage de contrôle sur le nombre de connexions utilisées.</span><span class="sxs-lookup"><span data-stu-id="39d6a-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39d6a-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39d6a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39d6a-119">Optimisation des interactions entre le niveau de logique métier COM+ et la couche présentation</span><span class="sxs-lookup"><span data-stu-id="39d6a-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



