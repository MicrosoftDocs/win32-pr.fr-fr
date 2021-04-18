---
description: La fonction PdhVbUpdateLog met à jour la requête actuelle et écrit de nouvelles données dans le fichier journal. Cette fonction appelle PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519900"
---
# <a name="pdhvbupdatelog-function"></a>PdhVbUpdateLog fonction)

La fonction **PdhVbUpdateLog** met à jour la requête actuelle et écrit de nouvelles données dans le fichier journal. Cette fonction appelle [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbUpdateLog ( \_ ByVal HLog en tant que PDH \_ hLog, \_ BYVAL szUserString As LPCTSTR \_ )

## <a name="parameters"></a>Paramètres

<dl> <dt>

*hLog* \[ dans\]
</dt> <dd>

Handle du fichier journal à mettre à jour. Ce descripteur est retourné par la fonction [**PdhVbOpenLog**](pdhvbopenlog.md) .

</dd> <dt>

*szUserString* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui spécifie les données à ajouter au fichier journal. Il est généralement utilisé pour les commentaires dans le fichier journal.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne 0.

Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md). Les valeurs possibles sont les suivantes.



| Code de retour                                                                                                | Description                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_mémoire tampon PDH insuffisante \_**</dt> </dl>   | Les données demandées sont supérieures à la mémoire tampon fournie. Impossible de retourner les données demandées.<br/> |
| <dl> <dt>**PDH \_ argument non valide \_**</dt> </dl>      | Une ou plusieurs des mémoires tampons de chaîne n’ont pas la taille correcte.<br/>                                  |
| <dl> <dt>**\_handle PDH non valide \_**</dt> </dl>        | Le descripteur n’est pas un objet PDH valide.<br/>                                                       |
| <dl> <dt>**\_erreur d' \_ ouverture du fichier journal \_ PDH \_**</dt> </dl> | Impossible d’ouvrir le fichier journal spécifié.<br/>                                                      |
| <dl> <dt>**\_fichier PDH \_ \_ introuvable**</dt> </dl>       | Impossible de trouver le fichier spécifié.<br/>                                                          |



 

## <a name="remarks"></a>Notes

Il doit y avoir une requête actuellement ouverte et les compteurs souhaités doivent y être ajoutés pour que cette fonction soit appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

