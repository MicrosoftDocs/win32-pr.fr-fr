---
title: /Error (commutateur)
description: Le commutateur/Error détermine les types de vérification des erreurs que les stubs générés exécuteront au moment de l’exécution.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- MIDL du commutateur/Error
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380892"
---
# <a name="error-switch"></a>/Error (commutateur)

Le commutateur **/Error** détermine les types de vérification des erreurs que les stubs générés exécuteront au moment de l’exécution.

> [!Note]  
> Cette fonctionnalité est obsolète et n’est plus prise en charge. L’utilisation du commutateur [**/Robust**](-robust.md) est recommandée.

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>allocation * * * *


</dt> <dd>

Vérifie si [**l' \_ \_ allocation d’utilisateur MIDL**](midl-user-allocate-1.md) retourne une valeur **null** , indiquant une erreur de mémoire insuffisante.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>\_données stub * * * *


</dt> <dd>

Génère un stub qui intercepte les exceptions d’annulation de marshaling côté serveur et les propage au client.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>Ref * * * * *


</dt> <dd>

Génère du code qui exécute une vérification au moment de l’exécution pour s’assurer qu’aucun pointeur de référence **null** n’est passé aux stubs du client et déclenche une \_ \_ \_ exception de pointeur Ref null RPC X \_ s’il en trouve.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>contrôle des limites \_ * * * *


</dt> <dd>

Vérifie la taille des tableaux variables et variables de conformité par rapport à la spécification de longueur de transmission.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>aucun * * * * *


</dt> <dd>

N’effectue aucune vérification des erreurs.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>tous les * * * *


</dt> <dd>

Effectue toutes les vérifications d’erreurs. Efficace avec MIDL version 5,0, il s’agit d’un commutateur de compilateur par défaut.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Le commutateur **/Error** sélectionne le nombre de vérifications d’erreurs effectuées par les fichiers stub générés. En vigueur avec MIDL version 5,0, le paramètre par défaut est **/Error All**.

Les erreurs d’énumération qui sont vérifiées (par défaut dans toutes les versions de MIDL) sont des erreurs de troncation provoquées lors de la conversion entre des types **enum longs** (entiers 32 bits) et des types **enum courts** (la représentation de données réseau de [**enum**](enum.md)) et le nombre d’identificateurs dans une énumération dépassant 32 767.

La vérification des erreurs d’accès à la mémoire (également par défaut dans toutes les versions de MIDL) concerne les pointeurs qui dépassent la fin de la mémoire tampon dans le code de marshaling et les tableaux conformes dont la taille est inférieure à zéro. Utilisez l’indicateur de **\_ vérification de limites/Error** pour rechercher d’autres limites de tableau non valides.

Lorsque vous spécifiez l' **allocation de/Error**, les stubs incluent du code qui lève une exception lorsque l' [**\_ utilisateur MIDL \_ allocate**](midl-user-allocate-1.md) retourne 0.

L’option de **\_ données de stub/Error** empêche les données du client de se bloquer sur le serveur pendant le démarshaling, ce qui offre une méthode plus robuste pour gérer l’opération de démarshaling.

Efficace avec WindowsÂ 2000, le moteur de marshaling des NDR à l’exécution sous-jacent effectue la plupart de ces contrôles. Cela signifie que si vous utilisez l’un des modes entièrement interprétés ([**/OI**](-oi.md), **/OIF**) de la génération du stub, le choix des options de vérification des erreurs différentes n’aura pas d’effet marqué sur les performances.

## <a name="examples"></a>Exemples

**attribution de l’attribution de nom de fichier. idl MIDL**

**MIDL/Error None nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




