---
title: Définition des extensions d’unité de données
description: Définition des extensions d’unité de données
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- extensions d’unité de données, définition
- flux, extensions d’unité de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521053"
---
# <a name="setting-data-unit-extensions"></a>Définition des extensions d’unité de données

Certains flux sont configurés pour utiliser des extensions d’unité de données pour associer des données supplémentaires à des échantillons individuels. Pour plus d’informations sur les exemples étendus, consultez [extensions d’unité de données](data-unit-extensions.md).

La plupart des systèmes d’extension d’unité de données requièrent une extension sur chaque échantillon dans le flux. Si vous ne fournissez pas une extension de la taille correcte, l’enregistreur rejettera l’exemple.

Pour ajouter des données étendues à un exemple, utilisez la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Vous pouvez obtenir des informations sur les extensions d’unité de données configurées sur un flux à l’aide des méthodes [**IWMStreamConfig2 :: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) et [**IWMStreamConfig2 :: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration d’extensions d’unité de données**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




