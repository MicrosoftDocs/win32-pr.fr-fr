---
title: Objet ClosedCaption
description: L’objet ClosedCaption offre un moyen d’inclure des sous-titres avec un clip multimédia. Le texte de sous-titrage se trouve dans un fichier SAMI (Synchronized Accessible Media Interchange).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Objet ClosedCaption lecteur Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104030455"
---
# <a name="closedcaption-object"></a>Objet ClosedCaption

L’objet **ClosedCaption** offre un moyen d’inclure des sous-titres avec un clip multimédia. Le texte de sous-titrage se trouve dans un fichier SAMI (Synchronized Accessible Media Interchange).

L’objet **ClosedCaption** prend en charge les propriétés suivantes.



| Propriété                                           | Description                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Spécifie ou récupère le nom du frame ou du contrôle qui affiche le sous-titrage.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Spécifie ou récupère le nom du fichier contenant les informations nécessaires pour le sous-titrage. |
| [SAMILang](closedcaption-samilang.md)             | Spécifie ou récupère la langue affichée pour le sous-titrage.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Récupère le nombre de langues prises en charge par le fichier SAMI actuel.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Spécifie ou récupère le style de sous-titrage.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Récupère le nombre de styles pris en charge par le fichier SAMI actuel.                                   |



 

L’objet **ClosedCaption** prend en charge les méthodes suivantes.



| Méthode                                                 | Description                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Récupère l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Récupère le nom d’une langue prise en charge par le fichier SAMI actuel.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Récupère le nom d’un style pris en charge par le fichier SAMI actuel.                        |



 

L’objet **ClosedCaption** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                                  |
|-----------------------------|-------------------------------------------|
| [Lecteur](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




