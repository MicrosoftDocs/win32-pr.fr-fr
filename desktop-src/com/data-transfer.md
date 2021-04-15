---
title: Transfert de données
description: Transfert de données
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507434"
---
# <a name="data-transfer"></a><span data-ttu-id="1fcf5-103">Transfert de données</span><span class="sxs-lookup"><span data-stu-id="1fcf5-103">Data Transfer</span></span>

<span data-ttu-id="1fcf5-104">Le modèle COM (Component Object Model) fournit un mécanisme standard pour transférer des données entre les applications.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="1fcf5-105">Ce mécanisme est l' *objet de données*, qui est tout simplement un objet com qui implémente l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="1fcf5-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="1fcf5-106">Certains objets de données, tels qu’un morceau de texte copié dans le presse-papiers, possèdent **IDataObject** comme seule interface.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="1fcf5-107">D’autres, telles que les objets de document composé, exposent plusieurs interfaces dont **IDataObject** est tout simplement un.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="1fcf5-108">Les objets de données sont fondamentaux pour le travail des documents composés, bien qu’ils aient également une application généralisée en dehors de cette technologie OLE.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="1fcf5-109">En échangeant des pointeurs vers un objet de données, les fournisseurs et les consommateurs de données peuvent gérer les transferts de données de manière uniforme, quel que soit le format des données, le type de support utilisé pour transférer les données ou l’appareil cible sur lequel ils doivent être rendus.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="1fcf5-110">Vous pouvez inclure la prise en charge dans votre application pour les transferts de base du presse-papiers, les transferts par glisser-déplacer et les transferts de documents composés OLE avec une seule implémentation de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="1fcf5-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="1fcf5-111">Cela fait, la quantité de code nécessaire pour prendre en charge la sémantique spéciale de chaque protocole est minime.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="1fcf5-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fcf5-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1fcf5-113">Interfaces Transfert de données</span><span class="sxs-lookup"><span data-stu-id="1fcf5-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="1fcf5-114">Formats de données et média de transfert</span><span class="sxs-lookup"><span data-stu-id="1fcf5-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="1fcf5-115">Glisser-déposer</span><span class="sxs-lookup"><span data-stu-id="1fcf5-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="1fcf5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fcf5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fcf5-117">Documents composés</span><span class="sxs-lookup"><span data-stu-id="1fcf5-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




