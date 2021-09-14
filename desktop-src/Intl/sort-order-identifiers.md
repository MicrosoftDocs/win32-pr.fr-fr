---
description: Cette rubrique décrit les identificateurs d’ordre de tri, qui peuvent être utilisés dans la préparation des identificateurs de paramètres régionaux.
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: Identificateurs d’ordre de tri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121881"
---
# <a name="sort-order-identifiers"></a>Identificateurs d’ordre de tri

Cette rubrique décrit les identificateurs d’ordre de tri, qui peuvent être utilisés dans la préparation des [identificateurs de paramètres régionaux](locale-identifiers.md). Un identificateur d’ordre de tri est défini sous la forme « \_ OrdreTri », à la fin du nom de paramètres régionaux utilisé dans l’identificateur, par exemple « de-de \_ phoneb », où « phoneb » est l’ordre de tri. L’identificateur de paramètres régionaux correspondant est créé comme suit : `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` .



| Constante                      | Nom des paramètres régionaux                                                                                         | Signification                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Trier en \_ chinois \_ Big5           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Ordre Chinois BIG5                                                |
| Trier en \_ chinois \_ bopomofo       | zh-TW \_ pronun                                                                                       | Ordre bopomofo chinois traditionnel                                |
| TRIER \_ l' \_ annuaire en chinois \_    | zh-CN \_ phoneb<br/>                                                                            | Commande de l’annuaire téléphonique chinois (nom)                                |
| TRIER \_ chinois \_ RPC            | zh- \_ trait CN<br/> le trait zh-HK \_<br/> le trait zh-MO \_<br/> le trait zh-SG \_<br/> | Ordre de décompte de traits PRC chinois                                    |
| TRI \_ chinois \_ PRCP           | zh-CN<br/> zh-SG<br/>                                                                   | Ordre phonétique PRC chinois                                        |
| TRI \_ chinois \_ RADICALSTROKE  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Clé chinoise/ordre des traits                                      |
| Trier en \_ chinois \_ Unicode        | —                                                                                                   | ordre Unicode chinois **Windows 2000 :** non pris en charge.<br/>  |
| TRIER \_ par défaut                 | Nom des paramètres régionaux qui est le même que le nom de la langue correspondante                                     | Ordre de tri par défaut                                                |
| SORT \_ géorgien \_ moderne        | Ka-GE \_ moderne                                                                                       | Commande géorgien moderne                                             |
| TRI \_ géorgien \_ traditionnel   | ka-GE                                                                                               | Ordre traditionnel géorgien                                        |
| TRIER \_ l' \_ \_ annuaire allemand     | de- \_ phoneb                                                                                       | Ordre des annuaires téléphoniques allemands                                           |
| TRIER \_ la \_ valeur par défaut hongroise      | hu-HU                                                                                               | Ordre hongrois par défaut                                           |
| TRI de la \_ technique hongroise \_    | HU-HU \_ technl                                                                                       | Commande technique hongroise                                         |
| TRI \_ japonais \_ RADICALSTROKE | ja-JP                                                                                               | Clé japonaise/ordre des traits                                     |
| TRIER \_ le \_ Unicode japonais       | —                                                                                                   | ordre Unicode japonais **Windows 2000 :** non pris en charge.<br/> |
| TRI \_ japonais \_ XJIS          | ja-JP                                                                                               | Ordre XJIS japonais                                               |
| TRI \_ coréen \_ KSC             | ko-KR                                                                                               | Ordre KSC coréen                                                  |
| TRIER \_ le \_ Unicode coréen         | —                                                                                                   | ordre Unicode coréen **Windows 2000 :** non pris en charge.<br/>   |



 

 

 




