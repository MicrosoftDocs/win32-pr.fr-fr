---
title: Ajout de caractères de copyright aux sous-fichiers
description: Les caractères pour les symboles de copyright et de marque déposée (\ 169 ; ou \ 174 ;) peuvent ne pas s’afficher correctement si le métafichier n’est pas encodé à l’aide du schéma d’encodage UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Ajout de caractères de copyright aux fichiers Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312505"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="be357-104">Ajout de caractères de copyright aux sous-fichiers</span><span class="sxs-lookup"><span data-stu-id="be357-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="be357-105">Les caractères des symboles de copyright et de marque déposée (© ou®) peuvent ne pas s’afficher correctement si le métafichier n’est pas encodé à l’aide du schéma d’encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="be357-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="be357-106">Dans ce cas, pour afficher correctement l’un de ces symboles pour tous les utilisateurs, vous pouvez utiliser les équivalents ASCII (c) et (r) à l’intérieur de l’élément de **Copyright** , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="be357-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="be357-107">Si le métafichier est encodé à l’aide de UTF-8, les symboles de copyright et de marque s’affichent correctement.</span><span class="sxs-lookup"><span data-stu-id="be357-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="be357-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be357-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be357-109">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="be357-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




