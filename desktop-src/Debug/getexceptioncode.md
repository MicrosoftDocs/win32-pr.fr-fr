---
description: Récupère un code qui identifie le type d’exception qui se produit. La fonction ne peut être appelée qu’à partir de l’expression de filtre ou du bloc de gestionnaire d’exceptions d’un gestionnaire d’exceptions.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: GetExceptionCode macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3b87b77ddb2d2e2af3a22e30d1204cf178ee6981
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114590"
---
# <a name="getexceptioncode-macro"></a>GetExceptionCode macro)

Récupère un code qui identifie le type d’exception qui se produit. La fonction ne peut être appelée qu’à partir de l’expression de filtre ou du bloc de gestionnaire d’exceptions d’un gestionnaire d’exceptions.

> [!Note]  
> Le compilateur d’optimisation Microsoft C/C++ interprète cette fonction comme un mot clé, et son utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur.

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Paramètres

Cette macro n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

La valeur de retour identifie le type d’exception. Le tableau suivant identifie les codes d’exception qui peuvent se produire en raison d’erreurs de programmation courantes. Ces valeurs sont définies dans WinBase. h et Winnt. h.



| Code de retour                                                                                                         | Description                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_violation d’accès à l’exception \_**</dt> </dl>         | Le thread tente de lire ou d’écrire dans une adresse virtuelle à laquelle il n’a pas accès.<br/> Cette valeur est définie en tant que violation d’accès d’état \_ \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**limites du tableau d’exceptions \_ \_ \_ dépassées**</dt> </dl>   | Le thread tente d’accéder à un élément de tableau qui est hors limites et le matériel sous-jacent prend en charge la vérification des limites.<br/> Cette valeur est définie en tant que limites de tableau d’état \_ \_ \_ dépassées.<br/>                                                                                                                 |
| <dl> <dt>**point d’arrêt d’EXCEPTION \_**</dt> </dl>                | Un point d’arrêt est rencontré.<br/> Cette valeur est définie en tant que point d’arrêt d’état \_ .<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**\_mauvais alignement de type de données d’exception \_**</dt> </dl>    | Le thread tente de lire ou d’écrire des données qui ne sont pas alignées sur le matériel qui ne fournit pas d’alignement. Par exemple, les valeurs 16 bits doivent être alignées sur des limites de 2 octets, des valeurs 32 bits sur des limites de 4 octets, et ainsi de suite.<br/> Cette valeur est définie en tant que \_ mauvais alignement de type de données d’état \_ .<br/>                    |
| <dl> <dt>**\_ \_ opérande dénormal de l’exception flt \_**</dt> </dl>    | L’un des opérandes d’une opération à virgule flottante est dénormal. Une valeur dénormalisée est une valeur qui est trop petite pour être représentée en tant que valeur à virgule flottante standard.<br/> Cette valeur est définie sous la forme d’un opérande d’état \_ float \_ Denormal \_ .<br/>                                                                                  |
| <dl> <dt>**EXCEPTION \_ flt \_ Division \_ par \_ zéro**</dt> </dl>     | Le thread tente de diviser une valeur à virgule flottante par un diviseur à virgule flottante de 0 (zéro).<br/> Cette valeur est définie en tant que valeur \_ float \_ d’état \_ par \_ zéro.<br/>                                                                                                                                               |
| <dl> <dt>**\_ \_ résultat inexact de l’exception flt \_**</dt> </dl>      | Le résultat d’une opération à virgule flottante ne peut pas être représenté exactement comme une fraction décimale.<br/> Cette valeur est définie sous la forme d’un résultat d’état \_ float \_ inexact \_ .<br/>                                                                                                                                                |
| <dl> <dt>**EXCEPTION \_ flt \_ non valide \_**</dt> </dl>   | Exception à virgule flottante qui n’est pas incluse dans cette liste.<br/> Cette valeur est définie comme une \_ \_ opération non valide d’État float \_ .<br/>                                                                                                                                                                             |
| <dl> <dt>**dépassement d’EXCEPTION \_ flt \_**</dt> </dl>             | L’exposant d’une opération à virgule flottante est supérieur à la magnitude autorisée par le type correspondant.<br/> Cette valeur est définie en tant \_ que \_ débordement de flotte d’État.<br/>                                                                                                                                         |
| <dl> <dt>**vérification de la pile de l’EXCEPTION \_ flt \_ \_**</dt> </dl>         | La pile a dépassé le dépassement de capacité négatif ou négatif, en raison d’une opération à virgule flottante.<br/> Cette valeur est définie en tant que \_ vérification de pile en virgule flottante d’état \_ \_ .<br/>                                                                                                                                                                 |
| <dl> <dt>**EXCEPTION \_ flt de dépassement de capacité \_ négatif**</dt> </dl>            | L’exposant d’une opération à virgule flottante est inférieur à la magnitude autorisée par le type correspondant.<br/> Cette valeur est définie sous la forme d’un dépassement de capacité négatif d’état \_ \_ .<br/>                                                                                                                                           |
| <dl> <dt>**\_page de garde des exceptions \_**</dt> </dl>               | Le thread a accédé à la mémoire allouée avec le \_ modificateur page Guard.<br/> Cette valeur est définie en tant que violation de page STATUs \_ Guard \_ \_ .<br/>                                                                                                                                                                          |
| <dl> <dt>**INSTRUCTION d’EXCEPTION \_ non conforme \_**</dt> </dl>      | Le thread tente d’exécuter une instruction non valide.<br/> Cette valeur est définie en tant qu' \_ instruction non conforme d’état \_ .<br/>                                                                                                                                                                                            |
| <dl> <dt>**EXCEPTION \_ dans \_ l' \_ erreur de page**</dt> </dl>           | Le thread tente d’accéder à une page qui n’est pas présente et le système ne peut pas charger la page. Par exemple, cette exception peut se produire si une connexion réseau est perdue lors de l’exécution d’un programme sur un réseau.<br/> Cette valeur est définie en tant qu’état \_ en cas d' \_ erreur de page \_ .<br/>                                   |
| <dl> <dt>**EXCEPTION \_ int \_ Division \_ par \_ zéro**</dt> </dl>     | Le thread tente de diviser une valeur entière par un diviseur entier de 0 (zéro).<br/> Cette valeur est définie en tant qu' \_ entier \_ d’État Division \_ par \_ zéro.<br/>                                                                                                                                                         |
| <dl> <dt>**\_dépassement de capacité int d’exception \_**</dt> </dl>             | Le résultat d’une opération d’entier crée une valeur qui est trop grande pour être conservée par le registre de destination. Dans certains cas, cela entraîne une opération de réalisation du bit le plus significatif du résultat. Certaines opérations ne définissent pas l’indicateur Carry.<br/> Cette valeur est définie en tant que dépassement de l’entier d’état \_ \_ .<br/> |
| <dl> <dt>**DISPOSITION d’EXCEPTION \_ non valide \_**</dt> </dl>      | Un gestionnaire d’exceptions retourne une disposition non valide au répartiteur d’exceptions. Les programmeurs qui utilisent un langage de haut niveau tel que C ne doivent jamais rencontrer cette exception.<br/> Cette valeur est définie en tant que \_ disposition non valide de l’état \_ .<br/>                                                                      |
| <dl> <dt>**HANDLE d’EXCEPTION \_ non valide \_**</dt> </dl>           | Le thread a utilisé un handle vers un objet de noyau qui n’était pas valide (probablement parce qu’il a été fermé).<br/> Cette valeur est définie en tant \_ que \_ descripteur d’État non valide.<br/>                                                                                                                                                 |
| <dl> <dt>**Exception qui ne pouvait pas être persistante \_ \_**</dt> </dl> | Le thread tente de poursuivre l’exécution après une exception qui ne peut pas être poursuivie.<br/> Cette valeur est définie en tant qu’exception État non \_ continuable \_ .<br/>                                                                                                                                                       |
| <dl> <dt>**\_instruction priv d’exception \_**</dt> </dl>         | Le thread tente d’exécuter une instruction avec une opération qui n’est pas autorisée dans le mode ordinateur actuel.<br/> Cette valeur est définie en tant qu' \_ instruction privilégiée d’état \_ .<br/>                                                                                                                           |
| <dl> <dt>**\_étape unique d’exception \_**</dt> </dl>              | Une interruption de trace ou un autre mécanisme d’instruction unique signale qu’une instruction est exécutée.<br/> Cette valeur est définie en tant qu’étape d’état \_ unique \_ .<br/>                                                                                                                                                           |
| <dl> <dt>**dépassement de capacité de la \_ pile \_**</dt> </dl>           | Le thread utilise sa pile.<br/> Cette valeur est définie en tant que dépassement de capacité de la pile d’état \_ \_ .<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**consolider le déroulement d’état \_ \_**</dt> </dl>          | Une consolidation de frame a été exécutée.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Notes

La fonction **GetExceptionCode** peut être appelée uniquement à partir de l’expression de filtre ou du bloc de gestionnaire d’exceptions d’un gestionnaire d’exceptions. L’expression de filtre est évaluée si une exception se produit pendant l’exécution du bloc **\_ \_ try** et détermine si le bloc **\_ \_ except** est exécuté ou non.

L’expression de filtre peut appeler une fonction de filtre. La fonction de filtre ne peut pas appeler **GetExceptionCode**. Toutefois, la valeur de retour de **GetExceptionCode** peut être transmise en tant que paramètre à une fonction de filtre. La valeur de retour de la fonction [**GetExceptionInformation**](getexceptioninformation.md) peut également être transmise en tant que paramètre à une fonction de filtre. **GetExceptionInformation** retourne un pointeur vers une structure qui comprend les informations de code de l’exception.

Lorsqu’il existe des gestionnaires imbriqués, chaque expression de filtre est évaluée jusqu’à ce qu’elle soit évaluée comme un gestionnaire d’exécution d’EXCEPTION \_ \_ ou une exception \_ continue \_ l’exécution. Chaque expression de filtre peut appeler **GetExceptionCode** pour recevoir le code de l’exception.

Le code d’exception retourné est le code généré par une exception matérielle, ou le code spécifié dans la fonction [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) pour une exception générée par le logiciel.

Lors de la gestion de l’exception de point d’arrêt, il est important d’incrémenter le pointeur d’instruction dans l’enregistrement de contexte pour continuer à partir de cette exception.

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [utilisation d’un gestionnaire d’exceptions](using-an-exception-handler.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Fonctions de gestion structurée des exceptions](structured-exception-handling-functions.md)
</dt> <dt>

[Vue d’ensemble de la gestion structurée des exceptions](structured-exception-handling.md)
</dt> </dl>

 

 
