---
title: commutateur/Robust
description: Le commutateur/Robust indique au compilateur MIDL de générer des informations supplémentaires de vérification des erreurs, que le moteur de NDR utilise pour effectuer des vérifications d’intégrité au moment de l’exécution.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- MIDL du commutateur/Robust
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551f5a60013aa3a903dcb3e35cc4c25a9f83dc67fff2a6ab5c7bfd62a041feee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895819"
---
# <a name="robust-switch"></a>commutateur/Robust

Le commutateur **/Robust** indique au compilateur MIDL de générer des informations supplémentaires de vérification des erreurs, que le moteur de NDR utilise pour effectuer des vérifications d’intégrité au moment de l’exécution.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/OIF* 
</dt> <dd>

Ces commutateurs sont identiques dans leurs fonctionnalités. Ils spécifient la méthode de proxy en mode Code du marshaling et utilisent des chaînes de format rapide pour améliorer les performances. Voir/ [**OI**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’utilisation du commutateur **/Robust** génère des informations supplémentaires qui permettent au moteur de représentation de données réseau d’effectuer une vérification des erreurs au moment de l’exécution sur des arguments corrélés dans des tableaux dynamiques, des unions et des pointeurs d’interface [**out**](out-idl.md) dans des applications DCOM. Le commutateur **/Robust** est uniquement disponible sous WindowsÂ 2000 et les versions ultérieures de Windows.

Un argument corrélé est un argument qui utilise l’un des attributs qui permettent de déterminer la taille d’un objet de données au moment de l’exécution : la [**taille \_ est**](size-is.md), la [**longueur \_ est**](length-is.md), le premier est, le [**dernier \_ est**](last-is.md), le [**nombre maximal \_**](max-is.md), le [**commutateur \_**](switch-is.md)et [**IID la \_ valeur**](iid-is.md). [**\_**](first-is.md) Conformément à la spécification OSF-DCE pour la représentation filaire, cet argument corrélé apparaît à deux emplacements différents. Par exemple, considérons une utilisation classique de la taille : attribute : **\_**

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

Dans cet exemple, le client passe une valeur long qui spécifie la taille d’un bloc de types de barres \_ (en termes de nombre d' \_ éléments de type barre) et un pointeur vers le bloc de types de barres réel \_ . L’argument Size est corrélé avec l’argument pBarType. Conformément à la spécification OSF-DCE, l’argument de taille est représenté deux fois sur le câble, d’abord comme lui-même, puis avec le tableau d’éléments de type de barre \_ qui représentent l’argument pBarType. Chaque argument est démarshalé indépendamment, en fonction de sa propre représentation filaire. Normalement, l’argument de taille et sa copie, qui est utilisée pour représenter une partie de l’autre argument, ont les mêmes valeurs. Toutefois, si l’argument de taille est endommagé (par exemple, lorsque le bloc de types de barres \_ est plus grand que ce qui a été alloué), l’application serveur peut cesser de répondre, car elle utilise la valeur de l’argument size pour mesurer les données entrantes.

Le commutateur **/Robust** est requis pour implémenter une vérification de plage valide avec l’attribut de [**plage**](range.md) .

## <a name="examples"></a>Exemples

**MIDL/Robust/Oicf NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**vont**](range.md)
</dt> </dl>

 

 




