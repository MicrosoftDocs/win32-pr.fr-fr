---
title: Stratégies de gestion des erreurs
description: Stratégies de gestion des erreurs
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0527edbb8bab4b4a0b0ca9e0d135bc5cf8c2827497a36fb9cad021680868f764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029969"
---
# <a name="error-handling-strategies"></a>Stratégies de gestion des erreurs

Étant donné que les méthodes d’interface sont virtuelles, il n’est pas possible pour un appelant de connaître l’ensemble des valeurs qui peuvent être retournées à partir d’un appel quelconque. Une implémentation d’une méthode peut retourner cinq valeurs ; un autre peut retourner huit.

La documentation répertorie les valeurs communes qui peuvent être retournées pour chaque méthode. Il s’agit des valeurs que vous devez vérifier et gérer dans votre code, car elles ont des significations particulières. D’autres valeurs peuvent être retournées, mais étant donné qu’elles ne sont pas significatives, vous n’avez pas besoin d’écrire un code spécial pour les gérer. Une vérification simple pour zéro ou une valeur différente de zéro est appropriée.

## <a name="hresult-values"></a>Valeurs HRESULT

La valeur de retour des fonctions et des méthodes COM est un **HRESULT**. Les valeurs de certains HRESULTs ont été modifiées dans COM pour éliminer toute duplication et se chevaucher avec les codes d’erreur système. Ceux qui dupliquent les codes d’erreur système ont été remplacés par l’installation de \_ Win32, et ceux qui se chevauchent restent \_ null. Les valeurs **HRESULT** communes et leurs valeurs sont répertoriées dans le tableau suivant.



| HRESULT                    | Valeur                 | Description                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ Abort<br/>        | 0x80004004<br/> | L’opération a été abandonnée en raison d’une erreur non spécifiée.<br/>                                                                              |
| \_ACCESSDENIED E<br/> | 0x80070005<br/> | Une erreur générale d’accès refusé.<br/>                                                                                                          |
| E \_ échec<br/>         | 0x80004005<br/> | Une erreur non spécifiée s’est produite.<br/>                                                                                                    |
| \_handle E<br/>       | 0x80070006<br/> | Un descripteur non valide a été utilisé.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Un ou plusieurs arguments ne sont pas valides.<br/>                                                                                                      |
| E \_ NOinterface<br/>  | 0x80004002<br/> | La méthode [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) n’a pas reconnu l’interface demandée. L’interface n’est pas prise en charge.<br/> |
| \_NOTIMPL E<br/>      | 0x80004001<br/> | Cette méthode n'est pas implémentée.<br/>                                                                                                          |
| \_OUTOFMEMORY E<br/>  | 0x8007000E<br/> | La méthode n’a pas pu allouer la mémoire nécessaire.<br/>                                                                                         |
| E \_ en attente<br/>      | 0x8000000A<br/> | Les données nécessaires à l’exécution de l’opération ne sont pas encore disponibles.<br/>                                                                      |
| \_pointeur E<br/>      | 0x80004003<br/> | Un pointeur non valide a été utilisé.<br/>                                                                                                            |
| E \_ inattendu<br/>   | 0x8000FFFF<br/> | Une défaillance catastrophique s’est produite.<br/>                                                                                                    |
| S \_ false<br/>        | 0x00000001<br/> | La méthode a réussi et a retourné la valeur booléenne **false**.<br/>                                                                          |
| \_OK<br/>           | 0x00000000<br/> | S_OK Si une valeur de retour booléenne est attendue, la valeur retournée est **true**.<br/>                                            |



 

## <a name="network-errors"></a>Erreurs réseau

Si les quatre premiers chiffres du code d’erreur sont 8007, cela indique une erreur système ou réseau. Vous pouvez utiliser la commande **net** pour décoder ces types d’erreurs. Pour décoder l’erreur, commencez par convertir les quatre derniers chiffres du code d’erreur hexadécimal en décimal. Ensuite, à l’invite de commandes, tapez ce qui suit, où le code décimal est remplacé par la valeur de retour que vous souhaitez décoder :

**net helpmsg <** _\_ Code décimal_*_>_*

La commande net renvoie une description de l’erreur. Par exemple, si COM retourne l’erreur 8007054B, convertissez 054B en Decimal (1355). Tapez ensuite la commande suivante :

**net helpmsg 1355**

La commande net retourne la description de l’erreur : « le domaine spécifié n’existe pas ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> </dl>

 

 





