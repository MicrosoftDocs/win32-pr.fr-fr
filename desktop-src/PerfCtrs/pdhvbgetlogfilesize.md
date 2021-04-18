---
description: La fonction PdhVbGetLogFileSize retourne la taille du fichier journal spécifié. Cette fonction appelle PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536156"
---
# <a name="pdhvbgetlogfilesize-function"></a>PdhVbGetLogFileSize fonction)

La fonction **PdhVbGetLogFileSize** retourne la taille du fichier journal spécifié. Cette fonction appelle [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbGetLogFileSize ( \_ ByVal HLog en tant que PDH \_ hLog, \_ ByRef llSize As long \_ ) As DWORD

## <a name="parameters"></a>Paramètres

<dl> <dt>

*hLog* \[ dans\]
</dt> <dd>

Handle du fichier journal. Ce descripteur est retourné par la fonction [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .

</dd> <dt>

*llSize* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille du fichier journal, en octets.

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



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

