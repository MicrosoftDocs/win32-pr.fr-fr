---
description: CryptoAPI a été conçu pour être facilement extensible. Les nouveaux types et paramètres peuvent être définis par n’importe quel auteur de fournisseur de services de chiffrement (CSP) pour que CryptoAPI plie les exigences d’un large éventail de situations.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Extension de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0538e15f49e61dc26cacd4e81c42dd462aec092877428ebe865ab97c7729f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007017"
---
# <a name="extending-cryptoapi"></a>Extension de CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) a été conçu pour être facilement extensible. Les nouveaux types et paramètres peuvent être définis par n’importe quel auteur de [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour que CryptoAPI plie les exigences d’un large éventail de situations.



| Éléments extensibles                                                                                                 | Commentaire                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Types de fournisseur<br/>                                                                                        | Un type de fournisseur représente une famille particulière ou un type de services de chiffrement. De nouveaux types de fournisseurs peuvent être définis, chacun desservant une niche particulière.<br/>                                                                                                                                                                                                                                                                                          |
| Paramètres du fournisseur<br/>                                                                                   | Les paramètres de fournisseur sont envoyés et reçus à l’aide de [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) et [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**), respectivement. De nouveaux paramètres de fournisseur pourraient permettre à un CSP d’être configuré de manière non prévue par les concepteurs CryptoAPI.<br/>                                                                                                                                                                 |
| Identificateurs d’algorithme<br/>                                                                                 | Les fonctions d’énumération de [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**) permettent aux applications de répertorier les identificateurs d’algorithme dynamiquement. De nouveaux algorithmes de [*hachage*](../secgloss/h-gly.md) , de [*clé publique*](../secgloss/p-gly.md)et [*symétrique*](../secgloss/s-gly.md)peuvent être définis à tout moment.<br/> |
| Types de paire de clés publique/[*privée*](../secgloss/p-gly.md)<br/> | Alors que de nouveaux types de paire de clés peuvent être définis en fonction des besoins, seules les [*paires de clés*](../secgloss/e-gly.md) de signature et d’échange de clés sont utilisées actuellement.<br/>                                                                                                                                                                                                                                           |
| Types BLOB de clé<br/>                                                                                        | Les nouveaux types d' [*objets BLOB*](../secgloss/b-gly.md) de clé peuvent permettre l’échange des clés de session, des clés publiques et des paires de clés publiques/privées de manière flexible à l’aide des fonctions [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) et [**CPImportKey**](https://www.bing.com/search?q=**CPImportKey**) .<br/>                                                                                                                                            |
| Paramètres clés<br/>                                                                                        | Les paramètres de clé sont envoyés et récupérés à l’aide de [**CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) et [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**). De nouveaux paramètres de clé peuvent permettre la prise en charge de nombreux types de clés différents.<br/>                                                                                                                                                                                                                         |
| Paramètres de l’objet de hachage<br/>                                                                                | Les paramètres de l’objet de hachage sont envoyés et récupérés à l’aide de [**CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) et [**CPGetHashParam**](https://www.bing.com/search?q=**CPGetHashParam**). De nouveaux paramètres d’objet de hachage peuvent permettre la prise en charge de nombreux types de [*hachages*](../secgloss/h-gly.md)différents.<br/>                                                                                                                                         |
| Valeurs d’indicateur<br/>                                                                                           | La plupart des fonctions CryptoAPI/CryptoSPI ont un paramètre *dwFlags* . Les nouvelles valeurs *dwFlags* peuvent modifier le comportement des fonctions si nécessaire.<br/>                                                                                                                                                                                                                                                                                                       |



 

Les extensions à CryptoAPI doivent être effectuées de manière responsable. Avant de définir de nouveaux paramètres et types d’algorithmes, un développeur CSP doit consulter Microsoft Corporation, afin que :

-   Les extensions CryptoAPI communes peuvent être identifiées et placées dans le fichier Wincrypt. h standard.
-   Les conflits d’espaces de noms peuvent être évités.
-   Il peut être déterminé si l’extension est requise ou si une opération particulière peut être obtenue à l’aide de l’API actuelle.

> [!Note]  
> Pour qu’un CSP soit compatible avec les applications développées pour le fournisseur de services de chiffrement de base Microsoft, il doit prendre en charge tous les éléments précédents, comme décrit dans [fonctions de chiffrement de base](cryptography-functions.md) et [fonctions du fournisseur de services de chiffrement](cryptography-functions.md).

 

 

 
