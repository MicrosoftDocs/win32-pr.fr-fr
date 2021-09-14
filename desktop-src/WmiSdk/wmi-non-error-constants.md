---
description: Les codes de retour WMI qui indiquent l’État et n’indiquent pas d’erreur.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes WMI non-erreur (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918668"
---
# <a name="wmi-non-error-constants"></a>Constantes non-erreur WMI

Les codes de retour WMI qui indiquent l’État et n’indiquent pas d’erreur.

Si une opération ne génère pas d’erreur, WMI retourne l’un des codes suivants sous la forme d’un **HRESULT** qui indique l’état de l’opération.

> [!Note]  
> Certaines méthodes des classes WMI peuvent retourner des codes d’erreur système et réseau (64, par exemple). Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes. Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.

 

en C++, vous pouvez appeler [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) et spécifier le module de message **C : \\ Windows \\ System32 \\ wbem \\wmiutils.dll** .

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ aucune \_ erreur**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



L'opération a réussi.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**\_faux S \_ WBEM**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Plus aucun objet n’est disponible, le nombre d’objets retournés est inférieur au nombre demandé, ou il s’agit de la fin d’une énumération. Cette valeur est également retournée lorsque cette méthode est appelée avec la valeur 0 pour le paramètre *uCount* .


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



Une tentative a été effectuée pour créer un objet ou une classe qui existe déjà.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_paramètres WBEM \_ \_ \_ par défaut**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Une propriété substituée a été supprimée. Cette valeur est retournée pour signaler que la valeur non substituée d’origine a été restaurée à la suite de la suppression.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ différent**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Les éléments (objets, classes, etc.) qui sont comparés ne sont pas identiques.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**délai de la WBEM \_ S \_**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Un appel a expiré. Il ne s’agit pas d’une condition d’erreur. Par conséquent, certains résultats peuvent avoir également été retournés.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ \_ n’a \_ plus de \_ données**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



Aucune donnée supplémentaire n’est disponible à partir de l’énumération, et l’utilisateur doit mettre fin à l’énumération.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**l’opération des S WBEM a été \_ \_ \_ annulée**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



L’opération a été intentionnellement ou non intentionnellement annulée.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ \_ en attente**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Une demande est toujours en cours et les résultats ne sont pas encore disponibles.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_objets WBEM \_ en double \_**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Plus d'une copie du même objet a été détectée dans le jeu de résultats d'une énumération.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_accès WBEM \_ S \_ refusé**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



L’utilisateur s’est vu refuser l’accès à certaines ressources, mais pas toutes.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ résultats PARTIELs \_ WBEM**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



L’utilisateur n’a pas reçu tous les objets demandés en raison de ressources inaccessibles (autres que des violations de sécurité).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_service WBEM S \_ Limited \_**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



Le fournisseur est en capacité de disposer d’un service limité.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ \_ mises à jour indirectement**
</dt> <dd> <dl> <dt>

274434 (0x43002)
</dt> <dt>



Réservé pour un usage futur.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de retour WMI](wmi-return-codes.md)
</dt> </dl>

 

