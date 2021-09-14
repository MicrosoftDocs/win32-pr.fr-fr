---
description: Définit les noms de l’utilisation de la clé étendue en fonction de l’emplacement où ils peuvent être utilisés.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Énumération CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121133"
---
# <a name="capicom_eku-enumeration"></a>CAPICOM \_ , énumération EKU

Le type d’énumération **\_ EKU** d’un CAPICOM définit les noms de l’utilisation de la clé étendue en fonction de l’endroit où ils peuvent être utilisés.

## <a name="members"></a>Membres



| Membre                                     | Description                                                                                                                                                 | Valeur |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_autre utilisation améliorée de la EKU \_**                    | Le certificat utilise le défini dans la stratégie locale. Utilisé si l’utilisation améliorée de la valeur requise n’est pas prédéfinie et que la valeur OID doit être définie par l’application.<br/> | 0     |
| **authentification du serveur de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**             | Le certificat peut être utilisé pour authentifier un serveur.<br/>                                                                                                | 1     |
| **authentification du client de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**             | Le certificat peut être utilisé pour authentifier un client.<br/>                                                                                                | 2     |
| **signature du code de l' \_ utilisation améliorée de la \_ \_ connexion**            | Le certificat peut être utilisé pour créer une signature numérique.<br/>                                                                                           | 3     |
| **\_protection par e-mail de l’utilisation améliorée de la \_ sécurité pour CAPICOM \_**        | Le certificat peut être utilisé pour la protection de la messagerie.<br/>                                                                                                    | 4     |
| **\_connexion par carte à \_ puce pour CAPICOM \_**         | Le certificat peut être utilisé pour l’ouverture de session par carte à puce. Introduit dans CAPICOM 2,0.<br/>                                                                         | 5     |
| **\_système de fichiers de \_ chiffrement \_ EKU \_ de CAPICOM** | Le certificat peut être utilisé pour EFS. Introduit dans CAPICOM 2,0.<br/>                                                                                      | 6     |



## <a name="remarks"></a>Notes

Le type d’énumération **\_ EKU CAPICOM** est utilisé par l' [**utilisation améliorée de la EKU. Propriété Name**](eku-name.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




