---
description: La fonction PdhVbOpenLog ouvre le fichier journal spécifié pour la lecture et l’écriture. Cette fonction appelle PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529115"
---
# <a name="pdhvbopenlog-function"></a>PdhVbOpenLog fonction)

La fonction **PdhVbOpenLog** ouvre le fichier journal spécifié pour la lecture et l’écriture. Cette fonction appelle [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Fonction PdhVbOpenLog ( \_ ByVal SzLogFileName en tant que LPCTSTR, \_ ByVal DWACCESSFLAGS comme DWORD, \_ BYVAL lpdwLogType comme LPDWORD, \_ ByVal hQuery comme PDH \_ HQUERY, \_ ByVal DwMaxSize comme DWORD, \_ ByVal SZUSERCAPTION comme LPCSTR, \_ ByRef phLog comme PDH \_ HLOG \_ ) comme DWORD

## <a name="parameters"></a>Paramètres

<dl> <dt>

*szLogFileName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui spécifie le nom du fichier journal à ouvrir.

Si le fichier journal contient des données SQL, le format du nom du fichier journal est **SQL :**_DataSourceName_*_!_* _Nom_fichier_journal_. Dans ce cas, la valeur du paramètre *lpdwLogType* est le \_ type de journal PDH \_ \_ SQL.

</dd> <dt>

*dwAccessFlags* \[ dans\]
</dt> <dd>

Type d’accès à spécifier lors de l’ouverture du fichier journal. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                   | Signification                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**\_ \_ accès en lecture \_ au Journal PDH**</dt> </dl>       | Un fichier journal est ouvert pour une opération de lecture.<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**\_accès en \_ écriture \_ au Journal PDH**</dt> </dl>    | Un nouveau fichier journal est ouvert pour une opération d’écriture.<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**PDH \_ - \_ accès à la mise à jour des journaux \_**</dt> </dl> | Un fichier journal existant est ouvert pour une opération d’écriture.<br/> |



 

La valeur sélectionnée dans le tableau précédent peut être combinée à l’aide de l’opérateur OR avec l’un des indicateurs d’accès Create suivants.



| Valeur                                                                                                                                                                                   | Signification                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**PDH \_ - \_ créer \_ un nouveau journal**</dt> </dl>          | Un nouveau fichier journal portant le nom spécifié est créé.<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**PDH \_ - \_ créer \_ toujours le journal**</dt> </dl> | Un nouveau fichier journal portant le nom spécifié est créé et tout fichier journal existant portant le même nom est effacé.<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**PDH \_ ouvrir le journal \_ \_ existant**</dt> </dl> | Un fichier journal existant portant le nom spécifié est ouvert. Si un fichier journal portant le nom spécifié n’existe pas, il est égal à PDH \_ log \_ Create \_ New.<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**PDH \_ ouvrir le journal \_ \_ toujours**</dt> </dl>       | Un fichier journal existant portant le nom spécifié est ouvert ou un nouveau fichier journal portant le nom spécifié est créé.<br/>                                          |



 

</dd> <dt>

*lpdwLogType* \[ dans\]
</dt> <dd>

Pointeur vers une variable qui indique le type de fichier journal à ouvrir. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                      | Signification                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**\_type de journal PDH \_ \_ non défini**</dt> </dl> | Format de fichier journal non défini.<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**\_type de journal PDH \_ \_ CSV**</dt> </dl>                   | Fichiers texte contenant des en-têtes de colonnes dans la première ligne et des exemples de données individuelles sur chaque ligne suivante.<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**\_type de journal PDH \_ \_ SQL**</dt> </dl>                   | Les données du fichier journal sont en SQL.<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**\_type de journal PDH \_ \_ TSV**</dt> </dl>                   | Identique au \_ type de journal PDH \_ \_ CSV.<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**\_type de journal PDH \_ \_ binaire**</dt> </dl>          | Format du fichier journal binaire. Contient des fichiers journaux circulaires.<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**\_type de journal PDH \_ \_ Perfmon**</dt> </dl>       | Format du fichier journal Perfmon.<br/>                                                                                     |



 

</dd> <dt>

*hQuery* \[ dans\]
</dt> <dd>

Handle de requête. Ce descripteur est retourné par la fonction [**PdhVbOpenQuery**](pdhvbopenquery.md) .

Ce paramètre peut avoir la **valeur null** si le fichier journal doit être ouvert en lecture.

</dd> <dt>

*dwMaxSize* \[ dans\]
</dt> <dd>

Taille maximale du fichier journal, en octets. Cette valeur est utilisée uniquement si le fichier journal est un fichier journal de taille limitée ou circulaire.

</dd> <dt>

*szUserCaption* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui spécifie la légende définie par l’utilisateur du fichier journal. Une légende de fichier journal décrit généralement le contenu du fichier journal. Lorsqu’un fichier journal existant est ouvert, la valeur de ce paramètre est ignorée.

</dd> <dt>

*phLog* \[ in, Ref\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un handle vers le fichier journal ouvert.

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

Lorsque vous utilisez cette fonction pour écrire des données de performances dans un fichier journal, vous devez d’abord ouvrir une requête à l’aide de [**PdhVbOpenQuery**](pdhvbopenquery.md).

Il doit y avoir une requête actuellement ouverte et les compteurs souhaités doivent y être ajoutés avant que cette fonction soit appelée.

Notez que les fichiers journaux au format Perfmon ne peuvent être ouverts que pour la lecture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

