---
description: Après avoir créé un document HTML source de page de référence des événements (ERP), vous devez le nommer pour que Moniteur réseau puisse l’afficher dans le observateur d’événements.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Attribution d’un nom à une page de référence d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194648"
---
# <a name="naming-an-event-reference-page"></a>Attribution d’un nom à une page de référence d’événement

Après avoir créé un document HTML source de page de référence des événements (ERP), vous devez le nommer pour que Moniteur réseau puisse l’afficher dans le observateur d’événements.

Analyse de nom et fichiers ERP expert au format suivant :

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**
</dt> <dd>

Nom du fichier DLL, à l’exclusion de l’extension de nom de fichier.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

Identificateur d’événement de l’expert ERP.

L’identificateur d’événement se trouve également dans le membre **EventIdent** de la structure **NMEVENTDATA** .

</dd> </dl>

Pour plus d’informations sur la création d’une ERP, consultez les rubriques suivantes :

-   [Création d’un expert et surveillance des pages de référence des événements](creating-expert-and-monitor-event-reference-pages.md)
-   [Écriture d’une page de référence d’événement](writing-an-event-reference-page.md)
-   [Test d’une page de référence d’événement](testing-an-event-reference-page.md)

 

 



