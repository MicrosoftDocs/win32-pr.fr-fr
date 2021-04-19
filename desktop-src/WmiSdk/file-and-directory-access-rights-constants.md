---
description: Les classes WMI qui représentent des fichiers ou des répertoires, tels que Win32 \_ CodecFile ou \_ un fichier de fichier CIM, contiennent une propriété AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de droits d’accès aux fichiers et aux répertoires (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545901"
---
# <a name="file-and-directory-access-rights-constants"></a>Constantes de droits d’accès aux fichiers et aux répertoires

Les classes WMI qui représentent des fichiers ou des répertoires, tels que [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) ou un [**fichier de \_ fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), contiennent une propriété **AccessMask** . Cette propriété contient des paramètres de bits qui spécifient les droits d’accès qu’un utilisateur ou un groupe doit avoir pour un accès ou des opérations spécifiques sur le fichier. Pour plus d’informations, consultez [sécurité des fichiers et droits d’accès](/windows/desktop/FileIO/file-security-and-access-rights) et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).

Les classes de fichiers ou de répertoires qui contiennent une propriété **AccessMask** sont les suivantes :

-   [**\_Fichier de fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**\_Répertoire CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**\_LOGICALFILE CIM**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**\_CodecFile Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**\_Répertoire Win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**\_NTEventLogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**\_Partage Win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**\_ShortcutFile Win32**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

La liste suivante répertorie les valeurs des droits d’accès aux fichiers et aux répertoires dans la propriété **AccessMask** . Cette propriété est une image bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_lire les \_ données de fichier**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Accorde le droit de lire des données à partir du fichier.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_Répertoire de liste de fichiers \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Accorde le droit de lire des données à partir du fichier. Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_données d’écriture de fichier \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Accorde le droit d’écrire des données dans le fichier.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**fichier \_ ajouter \_ un fichier**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Accorde le droit d’écrire des données dans le fichier. Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FICHIER \_ Ajouter des \_ données**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Accorde le droit d’ajouter des données au fichier. Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FICHIER \_ Ajouter un \_ sous-répertoire**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Accorde le droit d’ajouter des données au fichier. Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**lecture de fichier \_ \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Accorde le droit de lire les attributs étendus.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**écriture de fichier \_ \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Accorde le droit d’écrire des attributs étendus.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**exécution du fichier \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Accorde le droit d’exécuter un fichier.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**parcours de fichiers \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Accorde le droit d’exécuter un fichier. Pour un répertoire, le répertoire peut être parcouru.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_supprimer un \_ enfant de fichier**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_attributs de lecture de fichier \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Accorde le droit de lire les attributs du fichier.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_attributs d’écriture de fichier \_**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Accorde le droit de modifier les attributs de fichier.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**SUPPRIMER**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Accorde le droit de supprimer l’objet.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**LIRE \_ le contrôle**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Accorde le droit de lire les informations du descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ÉCRITURE \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Accorde le droit de modifier la liste DACL dans le descripteur de sécurité de l’objet pour l’objet.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**propriétaire en écriture \_**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Accorde le droit de modifier le propriétaire dans le descripteur de sécurité de l’objet.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**NON**
</dt> <dd> <dl> <dt>

1048576 ()
</dt> <dt>



Accorde le droit d’utiliser l’objet pour la synchronisation. Cela permet à un processus d’attendre jusqu’à ce que l’objet soit dans un état signalé. Certains types d’objets ne prennent pas en charge ce droit d’accès.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

