---
title: notifier l’attribut
description: L’attribut \ Notify \ demande au compilateur MIDL de générer un appel à une procédure \ Notify \ du côté serveur de l’application.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- l’attribut de notification MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093305"
---
# <a name="notify-attribute"></a>notifier l’attribut

L’attribut **\[ Notify \]** demande au compilateur MIDL de générer un appel à une procédure **\[ Notify \]** côté serveur de l’application.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom de la procédure* 
</dt> <dd>

Nom de la procédure distante à laquelle la procédure Notify sera associée.

</dd> </dl>

## <a name="remarks"></a>Notes

La procédure **\[ Notify \]** appelée à la suite de l’attribut **\[ Notify \]** est associée à une procédure distante particulière sur le serveur. Son concept est similaire à une fonction de rappel. Le stub appelle la procédure **\[ Notify \]** après que tous les arguments de sortie de la procédure distante à laquelle il est associé ont été marshalés et que toute mémoire associée aux paramètres soit libérée. La routine **\[ Notify \]** est appelée si un appel échoue avant l’exécution de la routine de serveur. Par exemple, si un serveur échoue pendant le démarshaling en raison de la réception de données incorrectes du client, la \[ \] routine Notify est appelée.

L’attribut **\[ Notify \]** est utile pour développer des applications acquérant des ressources dans des procédures distantes. Ces ressources sont ensuite libérées dans la procédure **\[ Notify \]** après que les paramètres de sortie de la procédure distante ont été entièrement marshalés.

Le nom de la procédure **\[ Notify \]** est le nom de la procédure distante suffixée par **\_ Notify**. La procédure **\_ Notify** ne nécessite aucun paramètre et ne retourne pas de résultat. Un prototype de cette procédure est également généré dans le fichier d’en-tête. Par exemple, si le fichier IDL contient les éléments suivants :

``` syntax
MyProcedure([in] short S);
```

Spécifiez ce qui suit dans le ACF pour MIDL pour générer l’appel de **\_ notification** :

``` syntax
[notify] MyProcedure();
```

Le compilateur MIDL génère le code stub du serveur qui contient l’appel suivant à la procédure **\_ Notify** :

``` syntax
MyProcedure_notify();
```

Le fichier d’en-tête contiendra un prototype :

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>Exemples

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> </dl>

 

 




