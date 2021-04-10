---
description: L’action RemoveIniValues supprime les informations de fichier. ini spécifiées pour la suppression dans la table RemoveIniFile si le composant est configuré pour être installé localement ou exécuté à partir de la source.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Action RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953005"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="c3735-103">Action RemoveIniValues</span><span class="sxs-lookup"><span data-stu-id="c3735-103">RemoveIniValues Action</span></span>

<span data-ttu-id="c3735-104">L’action RemoveIniValues supprime les informations de fichier. ini spécifiées pour la suppression dans la [table RemoveIniFile](removeinifile-table.md) si le composant est configuré pour être installé localement ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="c3735-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="c3735-105">L’action RemoveIniValues supprime les informations du fichier. ini qui ont été associées à un composant dans la [table inifile](inifile-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3735-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="c3735-106">Cette action supprime également les informations du fichier. ini si les informations ont été écrites par l' [action WriteIniValues](writeinivalues-action.md) et que la désinstallation du composant est planifiée.</span><span class="sxs-lookup"><span data-stu-id="c3735-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c3735-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="c3735-107">Sequence Restrictions</span></span>

<span data-ttu-id="c3735-108">L’action [InstallValidate](installvalidate-action.md) doit être appelée avant l’action RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="c3735-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="c3735-109">Si une action [WriteIniValues](writeinivalues-action.md) est utilisée dans la séquence, elle doit apparaître après RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="c3735-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c3735-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="c3735-110">ActionData Messages</span></span>



| <span data-ttu-id="c3735-111">Champ</span><span class="sxs-lookup"><span data-stu-id="c3735-111">Field</span></span> | <span data-ttu-id="c3735-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="c3735-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="c3735-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c3735-113">\[1\]</span></span> | <span data-ttu-id="c3735-114">Identificateur du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c3735-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="c3735-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c3735-115">\[2\]</span></span> | <span data-ttu-id="c3735-116">Section clé du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c3735-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="c3735-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="c3735-117">\[3\]</span></span> | <span data-ttu-id="c3735-118">Élément supprimé du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c3735-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="c3735-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="c3735-119">\[4\]</span></span> | <span data-ttu-id="c3735-120">Valeur supprimée du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c3735-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c3735-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3735-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3735-122">Table RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="c3735-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="c3735-123">Table IniFile</span><span class="sxs-lookup"><span data-stu-id="c3735-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="c3735-124">Action WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="c3735-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="c3735-125">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="c3735-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



