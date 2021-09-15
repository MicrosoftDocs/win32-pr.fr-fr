---
title: Valeurs de retour du gestionnaire (msctf. h)
description: Text Services Framework produit des valeurs de retour dans la plage comprise entre 0xHHHH0200 et 0xHHHH0507. Le tableau suivant indique aux responsables de renvoyer les valeurs par ordre alphabétique.
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea9c813f9ba71371f45e2475f73af4f3016e17b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311209"
---
# <a name="manager-return-values"></a>Valeurs de retour du gestionnaire

L’infrastructure de services de texte génère des valeurs de retour dans la plage de 0x *hhhh* 0200 à 0x *hhhh* 0507. Le tableau suivant indique aux responsables de renvoyer les valeurs par ordre alphabétique.

> [!Note]  
> Les descriptions fournies ne sont pas spécifiques ; la signification d’une valeur de retour peut varier en fonction de la méthode qui a retourné la valeur.

 



| Code/valeur de retour                                                                                                                                                                                                                                                   | Description                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**Tf \_ E \_ \_ existe déjà**</dt> <dt>0x80040506</dt> </dl>                   | La clé conservée est inscrite.<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**Tf \_ \_Composition E \_ rejetée**</dt> <dt>0x80040508</dt> </dl> | Le propriétaire du contexte a rejeté la composition.<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**Tf \_ E \_ 0x80040504 déconnectée**</dt> <dt></dt> </dl>                          | L’objet de contexte n’est pas sur une pile de documents.<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**Tf \_ \_EMPTYCONTEXT**</dt> <dt>0x80040509</dt> </dl>                          | Le contexte est vide.<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**Tf \_ \_Format E**</dt> <dt>0x8004020a</dt> </dl>                                            | Le propriétaire du contexte ne peut pas gérer les objets du type fourni par le paramètre pDataObject.<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**Tf \_ \_INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl>                          | Les coordonnées d’écran ne sont pas valides.<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**Tf \_ \_INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>                                | La position du caractère n’est pas valide.<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**Tf \_ \_INVALIDVIEW**</dt> <dt>0x80040505</dt> </dl>                             | L’affichage de contexte n’est pas valide.<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**Tf \_ E \_**</dt> <dt>0x80040500</dt> verrouillé </dl>                                            | Le contexte est déjà verrouillé.<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**Tf \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>                             | L’objet ne prend pas en charge l’interface demandée.<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**Tf \_ E \_ nodisposition**</dt> <dt>0x80040206</dt> </dl>                                      | La disposition du texte n’a pas été calculée.<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**Tf \_ 0x80040201 E \_ NOlock**</dt> <dt></dt> </dl>                                            | L’appelant n’a pas le type de document nécessaire.<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**Tf \_ E \_ noobject**</dt> <dt>0x80040202</dt> </dl>                                      | Il n’existe aucun objet incorporé à la position spécifiée.<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**Tf \_ 0x80040503 E \_ NOprocureur**</dt> <dt></dt> </dl>                                | Il n’existe aucun fournisseur de fonction pour la fonction spécifiée.<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**Tf \_ E \_ noselect**</dt> <dt>0x80040205</dt> </dl>                             | Aucune sélection n’existe dans le contexte.<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**Tf \_ E \_ noservice**</dt> <dt>0x80040203</dt> </dl>                                   | Le service spécifié n’existe pas ou ne peut pas être créé.<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**Tf \_ \_NOTOWNEDRANGE**</dt> <dt>0x80040502</dt> </dl>                       | Le gestionnaire TSF ne possède pas la plage.<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**Tf \_ \_Plage E \_ non \_ couverte**</dt> <dt>0x80040507</dt> </dl>         | La plage n’est pas comprise dans une composition active.<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**Tf \_ E \_ ReadOnly**</dt> <dt>0x80040209</dt> </dl>                                      | Le contexte d’édition est en lecture seule.<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**Tf \_ \_STACKFULL**</dt> <dt>0x80040501</dt> </dl>                                   | La pile de contexte est pleine.<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**Tf \_ 0x80040208 \_ synchrone E**</dt> <dt></dt> </dl>                             | Impossible d’obtenir un verrou synchrone en lecture seule.<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**Tf \_ S \_ Async**</dt> <dt>0x00040300</dt> </dl>                                               | Les données seront obtenues de manière asynchrone.<br/>                                              |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



 

 





