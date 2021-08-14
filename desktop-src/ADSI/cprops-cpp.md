---
title: CPROPS. COTISATIONS
description: Dans l’exemple de composant fournisseur, vous trouverez un exemple d’implémentation de cache de propriété dans cProps. cpp. Les méthodes prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66394b7375779f50a97505128178ec35106187c076ca5d6741375a7f71b8ec46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428998"
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



 

 

 




