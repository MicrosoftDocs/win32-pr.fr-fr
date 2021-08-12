---
title: Mappage de Active Directory syntaxe à la syntaxe ADSI
description: Le tableau suivant mappe les syntaxes de Active Directory à leurs syntaxes ADSI correspondantes.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- attributs ADSI, mappage Active Directory syntaxe à la syntaxe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04682a1e299e14c55c520310bff697ea6664d4dabe71380f7a146fd2dfff053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179277"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Mappage de Active Directory syntaxe à la syntaxe ADSI

Le tableau suivant mappe les syntaxes de Active Directory à leurs syntaxes ADSI correspondantes.



| ID de la syntaxe d’attribut | Type de syntaxe Active Directory             | Type de syntaxe ADSI équivalent                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Chaîne DN<br/>                     | Chaîne DN<br/>                                                |
| 2.5.5.2<br/>  | ID objet<br/>                     | Chaîne CaseIgnore<br/>                                        |
| 2.5.5.3<br/>  | Chaîne respectant la casse<br/>         | Chaîne CaseExact<br/>                                         |
| 2.5.5.4<br/>  | Chaîne case ignorée<br/>           | Chaîne CaseIgnore<br/>                                        |
| 2.5.5.5<br/>  | Imprimer la chaîne de cas<br/>             | Chaîne imprimable<br/>                                         |
| 2.5.5.6<br/>  | Chaîne numérique<br/>                | Chaîne numérique<br/>                                           |
| 2.5.5.7<br/>  | **Ou** Nom DNWithOctetString<br/> | Non pris en charge<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Integer<br/>                       | Integer<br/>                                                  |
| 2.5.5.10<br/> | Chaîne d’octets<br/>                  | Chaîne d’octets<br/>                                             |
| 2.5.5.11<br/> | Temps<br/>                          | Heure UTC<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Chaîne de cas ignore<br/>                                       |
| 2.5.5.13<br/> | Adresse<br/>                       | Non pris en charge<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Descripteur de sécurité NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Entier long<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Chaîne d’octets<br/>                                             |



 

 

 





