---
title: Propriétés et méthodes
description: Comme tout objet OLE, un contrôle fournit une grande partie de ses fonctionnalités via un ensemble d’interfaces entrantes avec des propriétés et des méthodes.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028877"
---
# <a name="properties-and-methods"></a><span data-ttu-id="a2560-103">Propriétés et méthodes</span><span class="sxs-lookup"><span data-stu-id="a2560-103">Properties and Methods</span></span>

<span data-ttu-id="a2560-104">Comme tout objet OLE, un contrôle fournit une grande partie de ses fonctionnalités via un ensemble d’interfaces entrantes avec des propriétés et des méthodes.</span><span class="sxs-lookup"><span data-stu-id="a2560-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="a2560-105">Un contrôle expose des propriétés et des méthodes via OLE Automation afin que les conteneurs puissent y accéder sous le contrôle d’un langage de programmation fourni par un conteneur.</span><span class="sxs-lookup"><span data-stu-id="a2560-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="a2560-106">Pour prendre en charge l’accès aux propriétés via une interface utilisateur, un contrôle fournit des pages de propriétés, la prise en charge des \_ Propriétés OLEIVERB, la navigation entre les propriétés et la liaison de données par le biais de la modification de propriété notifications.</span><span class="sxs-lookup"><span data-stu-id="a2560-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="a2560-107">Via les pages de propriétés, un contrôle peut afficher ses propriétés, indépendamment de son conteneur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a2560-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="a2560-108">En prenant en charge \_ les propriétés OLEIVERB, l’élément propriétés est affiché dans le menu du conteneur.</span><span class="sxs-lookup"><span data-stu-id="a2560-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="a2560-109">L’utilisateur final peut ensuite sélectionner l’élément **Propriétés** pour afficher les pages de propriétés du contrôle et modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="a2560-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="a2560-110">La navigation par propriété prend en charge un conteneur qui peut afficher les propriétés du contrôle dans le cadre d’une plus grande feuille de propriétés qui peut inclure des propriétés de plusieurs contrôles dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="a2560-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="a2560-111">Grâce à la notification de modification de propriété, un contrôle peut informer un client que ses propriétés ont changé, ce qui permet au client d’effectuer les actions nécessaires en conséquence.</span><span class="sxs-lookup"><span data-stu-id="a2560-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="a2560-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2560-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a2560-113">Propriétés du contrôle</span><span class="sxs-lookup"><span data-stu-id="a2560-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="a2560-114">Méthodes de contrôle</span><span class="sxs-lookup"><span data-stu-id="a2560-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="a2560-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2560-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2560-116">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="a2560-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="a2560-117">Pages de propriétés et feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="a2560-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




