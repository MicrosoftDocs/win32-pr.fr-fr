---
title: CGENOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, les méthodes d’objets génériques Active Directory, prises en charge dans cgenobj. cpp, sont répertoriées dans le tableau suivant.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe769dcfa6e4ab607188728115bcba16e40c0e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671178"
---
# <a name="cgenobjcpp"></a>CGENOBJ. COTISATIONS

Dans l’exemple de composant fournisseur, les méthodes d’objets génériques Active Directory, prises en charge dans cgenobj. cpp, sont répertoriées dans le tableau suivant.



| Méthode                                                                                  | Description                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Constructeur standard.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject :: ~ CSampleDSGenObject**                                             | Destructeur standard.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | Créez un objet générique ADS. Initialisez le cas échéant.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Créez cet objet dans son conteneur parent.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Enregistrez les propriétés de cet objet (effacez le cache).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Créez un objet générique et chargez ses données de type.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject :: QueryInterface**                                                  | Retourne le pointeur d’interface demandé, s’il est disponible.                                                                                                                                                                                                                                                                       |
| Méthodes [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard, y compris les implémentations de :                   | [**Obtient**](/windows/desktop/api/Iads/nf-iads-iads-get) (y compris le mappage du type de données natif au type Variant) [**put**](/windows/desktop/api/Iads/nf-iads-iads-put) (y compris le mappage du type Variant au type de données natif).<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (actualiser le cache de propriétés)<br/> [**Setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (enregistrer le cache de propriétés)<br/> |
| Méthodes [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) standard, y compris les implémentations de : | [](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**Récupération \_ \_** de la fonction GetObject](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**recevoir le \_ filtre**](iadscontainer-property-methods.md)<br/> [**Créés**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Supprimer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Routine utilitaire.                                                                                                                                                                                                                                                                                                            |



 

 

 





