---
title: Structure de IP_SPECIFIC_DATA (RTM. h)
description: La \_ structure de données spécifique à l’adresse IP contient des données spécifiques à IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA de la structure RAS
- Point d’accès RAS du pointeur de structure PIP_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104677"
---
# <a name="ip_specific_data-structure"></a>\_Structure de données spécifique à IP \_

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure de **\_ données spécifique à l’adresse IP** contient des données spécifiques à IP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Type FSD**
</dt> <dd>

Spécifie le type de routage tel que défini dans la [norme RFC 1354](routing-protocols-request-for-comments.md). Le tableau suivant indique les valeurs possibles pour ce membre.



| Membre                                                                                               | Signification                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Le type d’itinéraire n’est pas spécifié. Le type est différent de ceux répertoriés ici.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | L’itinéraire n’est pas valide. Normalement, cette valeur est utilisée pour invalider un itinéraire. Toutefois, étant donné que l’invalidation n’est pas prise en charge par le gestionnaire de tables de routage, l’itinéraire est toujours pris en compte dans les calculs les mieux routés. Par conséquent, les protocoles de routage ne doivent pas utiliser cette valeur.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | L’itinéraire est un itinéraire local, autrement dit, le tronçon suivant est la destination finale.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | L’itinéraire est un itinéraire distant, autrement dit, le tronçon suivant n’est pas la destination finale.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**\_Stratégie FSD**
</dt> <dd>

Spécifie l’ensemble de conditions qui provoquerait la sélection d’un itinéraire à plusieurs chemins d’accès. Ce membre est généralement au format TOS IP. Pour plus d’informations, consultez la [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ NextHopAS**
</dt> <dd>

Spécifie le numéro de système autonome du tronçon suivant.

</dd> <dt>

**\_Priorité FSD**
</dt> <dd>

Spécifie une valeur métrique. Le gestionnaire de tables de routage utilise cette valeur pour comparer cette entrée d’itinéraire aux entrées de routage obtenues à partir d’autres protocoles de routage. La valeur de ce membre est définie par le gestionnaire de tables de routage.

</dd> <dt>

**\_Métrique FSD**
</dt> <dd>

Spécifie une valeur métrique. Le gestionnaire de tables de routage utilise cette valeur pour comparer cette entrée d’itinéraire à d’autres entrées de routage obtenues à partir du même protocole de routage. La valeur de ce membre est définie par le protocole de routage.

</dd> <dt>

**FSD \_ Metric1**
</dt> <dd>

Spécifie une valeur métrique spécifique au protocole de routage. Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric2**
</dt> <dd>

Spécifie une valeur métrique spécifique au protocole de routage. Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric3**
</dt> <dd>

Spécifie une valeur métrique spécifique au protocole de routage. Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric4**
</dt> <dd>

Spécifie une valeur métrique spécifique au protocole de routage. Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ metric5)**
</dt> <dd>

Spécifie une valeur métrique spécifique au protocole de routage. Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**\_Indicateurs FSD**
</dt> <dd>

Spécifie si l’itinéraire est valide. Le protocole de routage doit d’abord effacer ces indicateurs, puis définir l’itinéraire comme étant valide ou non valide. Le protocole de routage doit utiliser les macros **ClearRouteFlags ()**, **SetRouteValid ()** et **ClearRouteValid ()** pour effectuer ces opérations. Ces macros sont définies dans RTM. h.

</dd> </dl>

## <a name="remarks"></a>Notes

Le gestionnaire de tables de routage utilise les membres **de \_ métriques** **FSD \_** et FSD pour calculer le meilleur itinéraire vers un réseau de destination particulier.

Les membres de la **\_ mesure FSD \[ 1-5 \]** sont conformes à la conformité MIB II. Les agents MIB II affichent uniquement ces valeurs de métriques. Ils n’affichent pas la valeur métrique de la **\_ mesure FSD** . Pour que la **\_ métrique FSD** soit affichée, le protocole de routage doit également stocker la valeur dans l’un des membres de la **\_ métrique FSD \[ 1-5 \]** .

Le gestionnaire de table de routage n’utilise pas les valeurs de métriques dans les membres de la **\_ mesure FSD \[ 1-5 \]** lors du calcul du meilleur itinéraire vers un réseau de destination. Par conséquent, le protocole de routage doit s’assurer que le membre de **\_ mesure FSD** a une valeur de métrique appropriée.

Un protocole de routage peut utiliser **les \_ indicateurs FSD** pour marquer un itinéraire comme étant non valide, si l’itinéraire ne doit pas être utilisé par d’autres protocoles de routage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Structures de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> </dl>

 

 





