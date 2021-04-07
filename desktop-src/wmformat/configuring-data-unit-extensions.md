---
title: Configuration d’extensions d’unité de données
description: Configuration d’extensions d’unité de données
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- flux, configuration des extensions d’unités de données
- flux, extensions d’unité de données
- extensions d’unité de données, configuration
- profils, extensions d’unité de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724047"
---
# <a name="configuring-data-unit-extensions"></a>Configuration d’extensions d’unité de données

Les exemples écrits dans des fichiers ASF peuvent contenir des informations supplémentaires, à l’exception des exemples de supports eux-mêmes. Ces informations sont incluses à l’aide d’extensions d’unité de données. Pour plus d’informations sur les extensions d’unité de données, consultez [extensions d’unité de données](data-unit-extensions.md).

Pour utiliser les extensions d’unité de données, vous devez configurer le flux de données dans le profil pour les accepter. Pour configurer une extension d’unité de données pour un flux, procédez comme suit.

1.  Obtenez un pointeur vers l’interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) en appelant la méthode **QueryInterface** de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).
2.  Appelez [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) pour inscrire un type d’extension d’unité de données pour le flux.

Vous pouvez examiner tous les types d’extension d’unité de données actuellement inscrits pour un flux en appelant [**IWMStreamConfig2 :: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) pour récupérer le nombre de types d’extension d’unité de données inscrits. Vous pouvez ensuite effectuer une boucle sur tous les types à l’aide d’appels à [**IWMStreamConfig2 :: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) pour chacun d’entre eux.

Une taille est attribuée aux extensions d’unité de données lorsqu’elles sont configurées pour un flux. De nombreux systèmes d’extension d’unité de données utilisent des données d’une taille constante (généralement une structure). Toutefois, vous pouvez également configurer vos extensions d’unité de données pour qu’elles soient de taille variable en définissant la taille sur 0xFFFF. Chaque extension d’unité de données affectée au moment de l’encodage peut être d’une taille quelconque comprise entre 1 octet et 65534 octets. Les extensions d’unité de données de taille variable sont également appelées extensions d’unité de données dynamiques.

L’avantage de l’utilisation des extensions d’unités de données dynamiques est que vous pouvez joindre des données d’extension en fonction des besoins. Si vous définissez une extension d’unité de données avec une taille définie, chaque échantillon du flux de données doit contenir des données d’extension de cette taille, même si vous n’avez pas de données pour certains exemples. Avec les extensions Dynamic Data Unit, vous pouvez omettre des extensions d’unité de données de certains exemples, ce qui économise de l’espace et réduit les besoins en bande passante. Toutefois, si les extensions d’unité de données sont de taille variable, l’objet de lecture ne peut pas vérifier les données d’extension reçues par rapport à une taille statique. Vous devez vérifier que les données d’extension que vous recevez sont valides, et qu’il ne s’agit pas d’une distorsion malveillante du flux de bits.

Les extensions d’unité de données individuelles doivent être définies sur des exemples à l’aide de la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Pour plus d’informations, consultez [définition des extensions d’unités de données](setting-data-unit-extensions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de flux**](configuring-streams.md)
</dt> </dl>

 

 




