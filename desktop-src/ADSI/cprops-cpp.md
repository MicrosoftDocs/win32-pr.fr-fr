---
title: CPROPS. COTISATIONS
description: Dans l’exemple de composant fournisseur, vous trouverez un exemple d’implémentation de cache de propriété dans cProps. cpp. Les méthodes prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839217"
---
# <a name="cpropscpp"></a>CPROPS. COTISATIONS

Dans l’exemple de composant fournisseur, vous trouverez un exemple d’implémentation de cache de propriété dans cProps. cpp. Les méthodes prises en charge sont répertoriées dans le tableau suivant.



| Méthode                                           | Description                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache :: AddProperty**                  | Étendez le cache des propriétés en ajoutant un nouveau.                                                                      |
| **CPropertyCache::updateproperty**               | Recherchez la propriété, libérez son contenu et utilisez de nouvelles valeurs à la place. Marquez ensuite le cache modifié pour cette propriété. |
| **CPropertyCache::findproperty**                 | Recherchez cette propriété par nom ; enregistrez son index.                                                                      |
| **CPropertyCache :: GetProperty**                  | Recherchez la propriété dans le cache si elle est disponible, sinon appelez **GetInfo**. Définissez l’index et copiez-les dans les nouvelles valeurs.  |
| **CPropertyCache ::p utproperty**                  | Recherchez la propriété. Libérez ce qui était là et placez les nouvelles valeurs.                                                       |
| **CPropertyCache::CPropertyCache**               | Constructeur standard.                                                                                               |
| **CPropertyCache :: ~ CPropertyCache**              | Destructeur standard.                                                                                                |
| **CPropertyCache::createpropertycache**          | Créez le cache.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Recherchez la propriété dans le cache et affectez-lui ces valeurs.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Marshaler les données et les valeurs de propriété.                                                                                   |
| **CPropertyCache::marshallproperty**             | Marshale une propriété.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Données et valeurs de propriété démarshalées.                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Démarshaler une propriété.                                                                                               |



 

 

 




