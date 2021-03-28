---
description: L’incorporation d’une police est la technique consistant à regrouper un document et les polices qu’il contient dans un fichier à transmettre à un autre ordinateur.
ms.assetid: ded409f1-5bd9-411b-b905-fc49c484786a
title: Polices incorporées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb8ab821afa5f44ded05a4a61a53439b8db9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114666"
---
# <a name="embedded-fonts"></a>Polices incorporées

L’incorporation d’une police est la technique consistant à regrouper un document et les polices qu’il contient dans un fichier à transmettre à un autre ordinateur. L’incorporation d’une police garantit qu’une police spécifiée dans un fichier transmis sera présente sur l’ordinateur recevant le fichier. Toutefois, toutes les polices ne peuvent pas être déplacées d’un ordinateur à l’autre, car la plupart des polices sont concédées sous licence pour un seul ordinateur à la fois. Seules les polices TrueType et OpenType peuvent être incorporées.

Les applications doivent incorporer une police dans un document uniquement lorsqu’elles sont demandées par un utilisateur. Une application ne peut pas être distribuée avec des documents qui contiennent des polices incorporées, de même qu’une application elle-même ne contient pas de police incorporée. Chaque fois qu’une application distribue une police, dans n’importe quel format, les droits de propriétaire du propriétaire de la police doivent être reconnus.

Il peut s’agir d’une violation des droits de propriété ou du contrat de licence utilisateur d’un fournisseur de polices pour incorporer des polices pour lesquelles l’incorporation n’est pas autorisée ou pour ne pas respecter les règles suivantes relatives à l’incorporation de polices. Une licence de police peut fournir uniquement une autorisation de lecture/écriture pour une police à installer et à utiliser sur l’ordinateur de destination. Ou la licence peut accorder une autorisation de lecture seule. L’autorisation lecture seule permet à un document d’être affiché et imprimé (mais pas modifié) par l’ordinateur de destination ; les documents avec des polices incorporées en lecture seule sont eux-mêmes en lecture seule. Les polices incorporées en lecture seule ne peuvent pas être dissociées du document et installées sur l’ordinateur de destination.

Une application peut déterminer l’état de la licence en appelant la fonction [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) et en examinant le membre **otmfsType** de la structure [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) . Si le bit 1 de **otmfsType** est défini, l’incorporation n’est pas autorisée pour la police. Si le bit 1 est clair, la police peut être incorporée. Si le bit 2 est défini, l’incorporation est en lecture seule.

Pour incorporer une police TrueType, une application peut utiliser la fonction [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata) pour lire le fichier de police. La définition des paramètres *dwTable* et *dwOffset* de [**GetFontData**](/windows/win32/api/wingdi/nf-wingdi-getfontdata) sur 0L et le paramètre *cbData* sur 1L garantit que l’application lit l’intégralité du fichier de police à partir du début.

Plusieurs fonctions sont disponibles pour incorporer les polices OpenType en fonction de la largeur des caractères et de l’emplacement des données de police. Pour incorporer une police Unicode OpenType qui réside dans un contexte de périphérique, une application peut utiliser [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont). Pour incorporer une police UCS-4 OpenType qui réside dans un contexte de périphérique, une application peut utiliser [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex). Pour incorporer une police Unicode OpenType qui réside dans un fichier de police, une application peut utiliser [**TTEmbedFontFromFile**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea). Pour plus d’informations sur l’incorporation de polices OpenType, consultez la [référence d’incorporation de polices](font-embedding-reference.md).

Une fois qu’une application a récupéré les données de police, elle peut stocker les données avec le document à l’aide de n’importe quel format applicable. La plupart des applications génèrent un répertoire de polices dans le document, en répertoriant les polices incorporées et si l’incorporation est en lecture/écriture ou en lecture seule. Une application peut utiliser les membres **otmpStyleName** et **otmFamilyName** de la structure [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) pour identifier la police.

Si le bit en lecture seule est défini pour la police incorporée, les applications doivent chiffrer les données de police avant de les stocker dans le document. La méthode de chiffrement n’a pas besoin d’être compliquée. par exemple, l’utilisation de l’opérateur XOR pour combiner les données de police avec une constante définie par l’application est appropriée et rapide.

 

 
