---
title: Vérification de l’inscription
description: Vérification de l’inscription
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501649"
---
# <a name="checking-registration"></a>Vérification de l’inscription

Chaque fois qu’une application est chargée, elle doit vérifier son inscription pour déterminer les éléments suivants :

-   Indique si les CLSID sont présents dans le registre. Si elles ne sont pas présentes, l’application doit s’inscrire en tant que programme d’installation d’origine.
-   Si les CLSID de l’application sont présents dans le registre, mais ne contiennent pas d’informations OLE 2. Si c’est le cas, l’application doit s’inscrire en tant que programme d’installation d’origine.
-   Indique si le chemin d’accès contenant des entrées de serveur ([LocalServer](localserver.md) et [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) et [InprocServer32](inprocserver32.md)et [DefaultIcon](defaulticon.md)) pointe vers l’emplacement où l’application est actuellement installée. Si le chemin d’accès ne le fait pas, réécrivez les entrées du chemin d’accès pour pointer vers l’emplacement actuel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> </dl>

 

 




