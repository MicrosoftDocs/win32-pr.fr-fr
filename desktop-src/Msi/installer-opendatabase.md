---
description: La méthode OpenDatabase de l’objet installer ouvre une base de données existante ou en crée une nouvelle, en retournant un objet Database. Elle génère une erreur si l’objet de base de données ne peut pas être créé et ouvert avec succès.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532916"
---
# <a name="installeropendatabase-method"></a>Installer. OpenDatabase, méthode

La méthode **OpenDatabase** de l’objet [**installer**](installer-object.md) ouvre une base de données existante ou en crée une nouvelle, en retournant un objet [**Database**](database-object.md) . Elle génère une erreur si l’objet **de base de données** ne peut pas être créé et ouvert avec succès.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*name* 
</dt> <dd>

Chaîne obligatoire qui contient le nom du chemin d’accès de la base de données. Si une chaîne vide est fournie, une base de données temporaire est créée, qui n’est pas persistante.

</dd> <dt>

*openMode* 
</dt> <dd>

Un paramètre de la liste suivante ou une chaîne qui contient le nom du chemin d’accès du nouveau fichier de base de données de sortie sur lequel l’écriture doit être effectuée lors de la validation.



| Paramètre                                                                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | Ouvre une base de données en lecture seule, pas de modifications persistantes.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | Ouvre une base de données en lecture/écriture en mode de transaction.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | Ouvre une base de données en lecture/écriture directe sans transaction.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | Crée une base de données, en lecture/écriture en mode Transact.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | Crée une base de données, en lecture/écriture en mode direct.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | Ouvre une base de données pour afficher les fichiers de script de publication, tels que les fichiers générés par la méthode [**CreateAdvertiseScript**](installer-createadvertisescript.md) .<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | Ajoute cet indicateur pour indiquer un fichier correctif.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsqu’une base de données est ouverte comme sortie d’une autre base de données, le flux d’informations de synthèse de la base de données de sortie est en fait un miroir en lecture seule de la base de données d’origine et ne peut donc pas être modifié. En outre, elle n’est pas conservée avec la base de données. Pour créer ou modifier les informations de résumé de la base de données de sortie, vous devez la fermer, puis la rouvrir.

Pour créer et enregistrer les modifications apportées à une base de données, commencez par ouvrir la base de données en mode transaction (msiOpenDatabaseModeTransact), Create (msiOpenDatabaseModeCreate ou msiOpenDatabaseModeCreateDirect) ou direct (msiOpenDatabaseModeDirect). Après avoir apporté les modifications, appelez toujours la méthode [**Commit**](database-commit.md) avant de fermer le handle de base de données. La méthode **Commit** vide toutes les mémoires tampons.

Appelez toujours la méthode [**Commit**](database-commit.md) sur une base de données qui a été ouverte en mode direct (MsiOpenDatabaseModeDirect ou msiOpenDatabaseModeCreateDirect) avant de fermer la base de données. L’échec de cette opération peut endommager la base de données.

Étant donné que la méthode **OpenDatabase** initie l’accès à la base de données, elle ne peut pas être utilisée avec une installation en cours d’exécution.

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




