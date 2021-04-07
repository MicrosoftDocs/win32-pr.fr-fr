---
title: Extensions d’unité de données
description: Extensions d’unité de données
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, Data Unit extensions
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- SDK Windows Media format, systèmes d’extension de charge utile
- ASF (Advanced Systems Format), systèmes d’extension de charge utile
- ASF (format de systèmes avancés), systèmes d’extension de charge utile
- extensions d’unité de données, à propos de
- extensions d’unité de charge utile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723498"
---
# <a name="data-unit-extensions"></a>Extensions d’unité de données

Le kit de développement logiciel (SDK) Windows Media format vous permet de compléter des données dans des exemples avec des *extensions d’unité de données*, également appelées systèmes d’extension de charge utile. Cette documentation utilise le terme « extensions d’unité de données » afin de rester cohérent avec les noms de méthode tels que [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension). Une extension d’unité de données est une paire nom/valeur attachée à l’exemple dans la section de données du fichier. Vous pouvez accéder aux données étendues à l’aide des méthodes de l’objet buffer lorsque l’exemple est récupéré par le lecteur.

Vous pouvez créer des extensions d’unité de données dans vos propres spécifications, mais plusieurs types sont prédéfinis et pris en charge par les objets de ce kit de développement logiciel (SDK). Ces extensions standard sont utilisées pour fournir des données supplémentaires pour les noms de fichiers (dans les flux de script et Web), les données de code temporel SMPTE, les proportions de pixels non carrés, la durée et le type d’entrelacement.

Pour utiliser les extensions d’unité de données, vous devez configurer le flux pour les accepter, puis ajouter des extensions à chaque exemple pour ce flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Configuration d’extensions d’unité de données**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Définition des extensions d’unité de données**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




