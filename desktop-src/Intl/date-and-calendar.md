---
description: Chaque paramètre régional est associé à un type de calendrier par défaut (type de données CALTYPE). Les paramètres régionaux peuvent également avoir un autre type de calendrier. Pour plus d’informations sur les types de calendriers, consultez informations sur le type de calendrier.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Date et calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f200ccd60a5a5d121a8774c01808794e744b98d8611210fcc98b0f8e5e1f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822809"
---
# <a name="date-and-calendar"></a>Date et calendrier

Chaque [paramètre régional](locales-and-languages.md) est associé à un type de calendrier par défaut (type de données CALTYPE). Les paramètres régionaux peuvent également avoir un autre type de calendrier. Pour plus d’informations sur les types de calendriers, consultez [informations sur le type de calendrier](calendar-type-information.md).

> [!Note]  
> Pour utiliser un autre type de calendrier pour des paramètres régionaux, votre application doit définir la constante [ \_ IOPTIONALCALENDAR des paramètres régionaux](locale-ioptionalcalendar.md) sur l’autre type de calendrier pour les paramètres régionaux.

 

La plupart des paramètres régionaux utilisent le calendrier grégorien standard et un nombre défini de formats de date. Ces choix par défaut pour les formats de date sont disponibles pour l’affichage à l’aide de la fonction [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) ou [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .

Certains paramètres régionaux requièrent des considérations particulières lors de la création d’une liste complète de choix de format. Certains de ces paramètres régionaux requièrent l’insertion de chaînes de texte dans la chaîne de format de date, tandis que d’autres nécessitent une méthode de calcul entièrement différente des valeurs. Une application répond à ces exigences spéciales par l’ajout de certains types d’informations de paramètres régionaux et de types de calendrier.

Pour plus d’informations sur l’implémentation de dates et de calendriers dans vos applications, consultez [récupération des informations de date et d’heure](retrieving-time-and-date-information.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la prise en charge linguistique nationale](about-national-language-support.md)
</dt> <dt>

[Informations sur le type de calendrier](calendar-type-information.md)
</dt> <dt>

[Récupération des informations de date et d’heure](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



