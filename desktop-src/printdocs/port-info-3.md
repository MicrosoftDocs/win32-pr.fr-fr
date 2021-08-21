---
description: La \_ structure d’informations sur le port \_ 3 spécifie la valeur d’état d’un port d’imprimante.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Structure PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cdd7f2fd931c7f503d566cdfc4ab38c5f595b51cea23d0cdf2fb326811cf7748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033967"
---
# <a name="port_info_3-structure"></a>Structure des informations de PORT \_ \_ 3

La structure d' **\_ informations sur le port \_ 3** spécifie la valeur d’état d’un port d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwStatus**
</dt> <dd>

Nouvelle valeur d’état de port. Cette valeur est utilisée uniquement si le membre **pszStatus** a la valeur **null**.

Ce membre peut être l’une des valeurs suivantes.



| Valeur                            | Signification                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Efface l’état du port d’imprimante.                     |
| État du PORT \_ \_ hors connexion            | L’imprimante du port est hors connexion.                      |
| \_ \_ bourrage papier dans l’état du port \_         | L’imprimante du port présente un bourrage papier.                 |
| \_ \_ sortie papier de l’état du port \_         | L’imprimante du port n’est plus imprimée.                 |
| bac de sortie de l’état du PORT \_ \_ \_ \_ plein  | Le bac de sortie printer’s du port est plein.            |
| problème de papier sur l’état du PORT \_ \_ \_     | L’imprimante du port présente un problème de papier.             |
| État du PORT \_ \_ non \_ toner          | L’imprimante du port est en dehors du toner.                 |
| porte d’état de PORT \_ \_ \_ ouverte         | La porte de l’imprimante du port est ouverte.             |
| INTERVENTION de l’utilisateur sur l’état du PORT \_ \_ \_ | L’imprimante du port nécessite une intervention de l’utilisateur.      |
| \_ \_ mémoire insuffisante sur l’état \_ du \_ port    | La mémoire de l’imprimante du port est insuffisante.                |
| \_toner état \_ \_ faible du port         | L’imprimante du port est faible sur le toner.                 |
| État du PORT en \_ \_ préchauffage \_        | L’imprimante du port est en état de préchauffage.                   |
| État du PORT-économie \_ \_ d’énergie \_        | L’imprimante du port est en mode de conservation de l’alimentation. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Pointeur vers une nouvelle chaîne de valeur d’état de port d’imprimante à définir. Utilisez ce membre s’il n’existe pas de valeur d’État appropriée parmi celles listées pour **dwStatus**.

</dd> <dt>

**dwSeverity**
</dt> <dd>

Gravité de la valeur de l’état du port.

Ce membre peut être l’une des valeurs suivantes.



| Valeur                       | Signification                                   |
|-----------------------------|-------------------------------------------|
| \_erreur de \_ type d’état de port \_   | La valeur de l’état du port indique une erreur. |
| \_avertissement de \_ type d’état de port \_ | La valeur de l’état du port est un avertissement.       |
| \_ \_ informations sur le type d’État du port \_    | La valeur de l’état du port est informatif.   |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous définissez une valeur d’état de port d’imprimante avec la valeur de gravité \_ \_ erreur de type état du port \_ , le spouleur d’impression cesse d’envoyer des travaux au port. Le spouleur d’impression ne reprend pas l’envoi des travaux au port jusqu’à ce qu’un autre appel [**SetPort**](setport.md) soit effectué pour effacer l’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le port 3W** (Unicode) et **\_ \_ informations sur le port \_ 3A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




