---
description: Architecture DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Architecture DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515523"
---
# <a name="dmo-architecture"></a>Architecture DMO

Cette section décrit l’architecture globale d’un DMO.

**Flux**

Un objet DMO est un objet qui prend des entrées *m* et produit *n* sorties. Les entrées et les sorties sont appelées des *flux*. Chaque DMO a au moins un flux. Les flux ne sont pas des objets ; ils sont simplement référencés sur le numéro d’index DMO. Le nombre de flux est défini au moment de la conception.

**Types de médias**

Toutes les données sont tapées à l’aide d’un *type de média*, qui définit comment interpréter le contenu des données. Par exemple, la vidéo RGB 320 x 240 24 bits est un type ; 44,1-kilohertz (kHz) audio stéréo 16 bits est un autre type. Les types de supports sont décrits à l’aide de la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Avant que le client puisse traiter des données, il doit définir le type de support pour chaque flux de données dans la méthode DMO.

En règle générale, un flux peut accepter une plage de types de médias. Certains DMOs prennent en charge un plus grand nombre de types que d’autres. Les interfaces DMO définissent les méthodes pour que le client Découvre les types pris en charge. Par exemple, un DMO peut prendre en charge la vidéo RVB en toute profondeur, tandis qu’un autre peut prendre en charge uniquement la couleur RVB 24 bits. En outre, un DMO peut être limité à certaines combinaisons d’entrées et de sorties. Par exemple, si le type d’entrée est vidéo 16 bits, le flux de sortie peut nécessiter la même profondeur de bit. Le client peut énumérer les types préférés de chaque flux, puis tester des combinaisons spécifiques.

**Mémoires tampons**

Dans le modèle DMO par défaut, le client alloue des mémoires tampons d’entrée et de sortie distinctes. Il remplit les tampons d’entrée avec les données et les remet à la solution DMO, et le DMO écrit de nouvelles données dans les mémoires tampons de sortie.

Si vous le souhaitez, un module DMO peut prendre en charge le traitement « sur place ». Avec le traitement sur place, DMO écrit la sortie directement dans la mémoire tampon d’entrée, sur les données d’origine. Le traitement sur place élimine la nécessité de mémoires tampons distinctes. D’un autre côté, il modifie les données d’origine, ce qui peut ne pas être acceptable pour certaines applications.

Le modèle de mise en mémoire tampon par défaut (non sur place) est pris en charge via l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Toutes les DMOs doivent implémenter cette interface. Si un module DMO prend en charge le traitement sur place, il expose également l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) . Le client est responsable de l’allocation de toutes les mémoires tampons, à la fois en entrée et en sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de DMOs](about-dmos.md)
</dt> </dl>

 

 



