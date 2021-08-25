---
Description: Les attributs de fichier sont des valeurs de métadonnées stockées par le système de fichiers sur disque et sont utilisés par le système et sont disponibles pour les développeurs via diverses API d’e/s de fichier.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Constantes d’attribut de fichier (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: 1dbb3d8e5eb091c47635f78eba9558a0d2262caeb5ce482c7b5bccdc3b237169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050869"
---
# <a name="file-attribute-constants"></a>Constantes d'attributs de fichier

Les attributs de fichier sont des valeurs de métadonnées stockées par le système de fichiers sur disque et sont utilisés par le système et sont disponibles pour les développeurs via diverses API d’e/s de fichier. Pour obtenir la liste des API et des rubriques connexes, consultez la section Voir aussi.

## <a name="example"></a>Exemple
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

exemple tiré d’un [exemple de Windows classique](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) sur GitHub.



| Constante/valeur                                                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**Fichier \_ \_Archive d’attributs**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Fichier ou répertoire qui est un fichier d’archive ou un répertoire. Les applications utilisent généralement cet attribut pour marquer des fichiers à des fins de sauvegarde ou de suppression. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ compressé**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Fichier ou répertoire compressé. Pour un fichier, toutes les données du fichier sont compressées. Pour un répertoire, la compression est la valeur par défaut pour les fichiers et les sous-répertoires nouvellement créés.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**Fichier \_ \_Appareil d’attribut**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Cette valeur est réservée à l’utilisation du système.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**Fichier \_ \_Répertoire d’attributs**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Handle qui identifie un répertoire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ chiffré**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Fichier ou répertoire chiffré. Pour un fichier, tous les flux de données du fichier sont chiffrés. Pour un répertoire, le chiffrement est la valeur par défaut pour les fichiers et sous-répertoires nouvellement créés.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ masqué**</dt> <dt>2 (0X2)</dt> </dl>                                                            | Le fichier ou le répertoire est masqué. Elle n’est pas incluse dans une liste de répertoires ordinaire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**Fichier \_ \_ \_ Flux d’intégrité de l’attribut**</dt> <dt>32768 (0x8000)</dt> </dl>                      | Le flux de données de l’annuaire ou de l’utilisateur est configuré avec l’intégrité (uniquement pris en charge sur les volumes ReFS). Elle n’est pas incluse dans une liste de répertoires ordinaire. Le paramètre d’intégrité persiste avec le fichier s’il est renommé. Si un fichier est copié, l’intégrité du fichier de destination est définie si l’intégrité du fichier source ou du répertoire de destination est définie.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cet indicateur n’est pas pris en charge tant que Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Fichier pour lequel d’autres attributs ne sont pas définis. Cet attribut n’est valide que lorsqu’il est utilisé seul.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ non \_ CONTENT \_ indexé**</dt> <dt>8192 (0x2000)</dt> </dl>             | Le fichier ou le répertoire ne doit pas être indexé par le service d’indexation de contenu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ no \_ SCRUB \_ Data**</dt> <dt>131072 (0x20000)</dt> </dl>                            | Le flux de données utilisateur ne doit pas être lu par le scanneur d’intégrité des données en arrière-plan (également appelé épurateur). Lorsqu’il est défini sur un répertoire, il fournit l’héritage uniquement. cet indicateur est uniquement pris en charge sur les volumes espaces de stockage et ReFS. Elle n’est pas incluse dans une liste de répertoires ordinaire.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** cet indicateur n’est pas pris en charge tant que Windows 8 et Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ hors connexion**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Les données d’un fichier ne sont pas immédiatement disponibles. Cet attribut indique que les données du fichier sont physiquement déplacées vers un stockage hors connexion. cet attribut est utilisé par le Stockage distant, qui est le logiciel de gestion de stockage hiérarchique. Les applications ne doivent pas modifier cet attribut de manière arbitraire.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ ReadOnly**</dt> <dt>1 (0x1)</dt> </dl>                                                      | Fichier en lecture seule. Les applications peuvent lire le fichier, mais ne peut pas y écrire ou le supprimer. Cet attribut n’est pas respecté sur les répertoires. pour plus d’informations, consultez [vous ne pouvez pas afficher ou modifier les attributs en lecture seule ou système des dossiers dans Windows Server 2003, dans Windows XP, dans Windows Vista ou dans Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**Fichier \_ \_Rappel \_ d’attribut \_ sur \_ l’accès aux données**</dt> <dt>4194304 (0x400000)</dt> </dl> | Lorsque cet attribut est défini, cela signifie que le fichier ou le répertoire n’est pas entièrement présent localement. Pour un fichier qui signifie que toutes ses données ne se trouvent pas sur le stockage local (par exemple, elles peuvent être éparses avec des données toujours dans le stockage distant). Pour un répertoire, cela signifie que certains contenus du répertoire sont virtualisés à partir d’un autre emplacement. La lecture du fichier/l’énumération du répertoire est plus coûteuse que la normale. par exemple, une partie du contenu de fichier/répertoire peut être extraite d’un magasin distant. Seuls les appelants en mode noyau peuvent définir ce bit.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**Fichier \_ \_Rappel \_ d’attribut sur \_ Open**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Cet attribut s’affiche uniquement dans les classes d’énumération de répertoire ( \_ informations sur les répertoires de fichiers \_ , fichiers de répertoire \_ \_ \_ , etc.). Lorsque cet attribut est défini, cela signifie que le fichier ou le répertoire n’a pas de représentation physique sur le système local. l’élément est virtuel. L’ouverture de l’élément est plus coûteuse que la normale. par exemple, il peut en résulter l’extraction d’au moins une partie de celui-ci à partir d’un magasin distant.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**Fichier \_ \_ \_ Point d’analyse d’attribut**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Fichier ou répertoire qui possède un point d’analyse associé, ou un fichier qui est un lien symbolique.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**Fichier \_ \_ \_ Fichier épars d’attribut**</dt> <dt>512 (0x200)</dt> </dl>                                        | Fichier qui est un fichier partiellement alloué.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**Fichier \_ \_Système d’attributs**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Fichier ou répertoire utilisé par le système d’exploitation, ou utilisé exclusivement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ temporaire**</dt> <dt>256 (0x100)</dt> </dl>                                               | Fichier utilisé pour le stockage temporaire. Les systèmes de fichiers évitent l’écriture de données dans le stockage de masse si une mémoire cache suffisante est disponible, car en général, une application supprime un fichier temporaire une fois le descripteur fermé. Dans ce scénario, le système peut entièrement éviter d’écrire les données. Dans le cas contraire, les données sont écrites après la fermeture du descripteur.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**Fichier \_ ATTRIBUT \_ virtuel**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Cette valeur est réservée à l’utilisation du système.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>winnt. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attribut de compression](compression-attribute.md)
</dt> <dt>

[Création et ouverture de fichiers](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




