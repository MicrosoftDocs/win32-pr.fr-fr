---
description: Récupère une description indépendante de l’ordinateur d’une exception et des informations sur l’état de l’ordinateur qui existe pour le thread lorsque l’exception se produit. Cette fonction ne peut être appelée qu’à partir de l’expression de filtre d’un gestionnaire d’exceptions.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 425cfbe10ac2ee66f10e016489ff070b67b6fc243a472f95b4f5809724998a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279219"
---
# <a name="getexceptioninformation-macro"></a>GetExceptionInformation macro)

Récupère une description indépendante de l’ordinateur d’une exception et des informations sur l’état de l’ordinateur qui existe pour le thread lorsque l’exception se produit. Cette fonction ne peut être appelée qu’à partir de l’expression de filtre d’un gestionnaire d’exceptions.

> [!Note]  
> Le compilateur d’optimisation Microsoft C/C++ interprète cette fonction comme un mot clé, et son utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur.

 

## <a name="syntax"></a>Syntaxe


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Paramètres

Cette macro n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Pointeur vers une structure [**de \_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) qui contient des pointeurs vers les deux structures suivantes :

-   [**Exception \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Structure d’enregistrement qui contient une description de l’exception.
-   Structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) qui contient les informations sur l’état de l’ordinateur.

## <a name="remarks"></a>Remarques

L’expression de filtre (à partir de laquelle la fonction est appelée) est évaluée si une exception se produit pendant l’exécution du bloc **\_ \_ try** et détermine si le bloc **\_ \_ except** est exécuté ou non.

L’expression de filtre peut appeler une fonction de filtre. La fonction de filtre ne peut pas appeler **GetExceptionInformation**. Toutefois, la valeur de retour de **GetExceptionInformation** peut être transmise en tant que paramètre à une fonction de filtre.

Pour passer les informations relatives aux [**\_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) au bloc de gestionnaire d’exceptions, l’expression de filtre ou la fonction de filtre doit copier le pointeur ou les données dans un stockage sécurisé auquel le gestionnaire peut accéder ultérieurement.

Dans le cas de gestionnaires imbriqués, chaque expression de filtre est évaluée jusqu’à ce qu’elle soit évaluée en tant que **\_ \_ Gestionnaire d’exécution d’exception** ou que **\_ l’exception continue \_ l’exécution**. Chaque expression de filtre peut appeler **GetExceptionInformation** pour recevoir des informations sur les exceptions.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CONTEXTE**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**\_pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**enregistrement d’EXCEPTION \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Fonctions de gestion structurée des exceptions](structured-exception-handling-functions.md)
</dt> <dt>

[Vue d’ensemble de la gestion structurée des exceptions](structured-exception-handling.md)
</dt> <dt>

[activer la prise en charge de Windows pour Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
