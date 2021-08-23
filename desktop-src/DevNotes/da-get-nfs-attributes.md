---
description: Le \_ Code de contrôle des attributs da obtenir \_ NFS \_ interroge des informations supplémentaires sur un partage NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Code de contrôle DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: e3e2b974d58888c35c24e18f16e1e75da46a180bb8123e9745170e074cd448de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956108"
---
# <a name="da_get_nfs_attributes-control-code"></a>\_Code de \_ contrôle des attributs NFS d’extraction de da \_

Le code de contrôle des **\_ \_ \_ attributs da obtenir NFS** interroge des informations supplémentaires sur un partage NFS.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* \[ dans\]
</dt> <dd>

Handle d’un fichier sur le partage NFS. Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ dans\]
</dt> <dd>

Code de contrôle de l’opération. Utilisez **da \_ obtenir \_ des \_ attributs NFS** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilisé avec cette opération ; Affectez la valeur **null**.

</dd> <dt>

*nInBufferSize* \[ dans\]
</dt> <dd>

Non utilisé avec cette opération ; défini à zéro.

</dd> <dt>

*lpOutBuffer* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon de sortie, qui contient une structure d' **\_ \_ attributs de fichier NFS** . Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*nOutBufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

</dd> <dt>

*lpBytesReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.

Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.

Si *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**. Même lorsqu’une opération ne retourne aucune donnée de sortie et que *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*. Après une telle opération, la valeur de *lpBytesReturned* est sans signification.

Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**. Si ce paramètre n’est pas **null** et que l’opération retourne des données, *lpBytesReturned* n’a pas de sens tant que l’opération avec chevauchement n’est pas terminée. Pour récupérer le nombre d’octets retournés, appelez [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.

Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement. Dans le cas contraire, la fonction échoue de façon imprévisible.

Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée. Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Ce code de contrôle n’a aucun fichier d’en-tête associé. Vous devez définir le code de contrôle et les structures de données comme suit.

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

Les membres de la structure peuvent être décrits comme suit.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Valeur opaque utilisée pour les types de fichiers spéciaux, tels que les fichiers spéciaux de bloc, spéciaux et FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Valeur opaque utilisée pour les types de fichiers spéciaux, tels que les fichiers spéciaux de bloc, spéciaux et FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Durée**
</dt> <dd>

Valeur 64 bits représentant les secondes écoulées depuis le 1er janvier 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

Nombre de nanosecondes à ajouter au membre **seconds** .

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**
</dt> <dd>

Type de fichier NFS du partage.



| Type de fichier NFS                                                                              | Description                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>\_reg de type NFS \_<br/>    | Fichier normal.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>Rép. de \_ type NFS \_<br/>    | Un répertoire.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_BLK de type NFS \_<br/>    | Fichier spécial de bloc.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>TYPE de NFS \_ \_ Chr<br/>    | Fichier spécial de caractères.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>\_type NFS \_ lnk<br/>    | Lien symbolique.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>\_chaussette de type NFS \_<br/> | socket Windows.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>\_type NFS \_ FIFO<br/> | Fichier FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**
</dt> <dd>

Mode de fichier.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

Nombre de liens vers le partage.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Codé**
</dt> <dd>

identificateur d’utilisateur (UID) UNIX.

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**ID**
</dt> <dd>

identificateur du groupe de UNIX (GID).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Corps**
</dt> <dd>

Taille du fichier, en octets.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Servir**
</dt> <dd>

Taille de fichier utilisée, en octets. Il s’agit de la même taille de fichier.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Identificateur de l’appareil.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

Identificateur du système de fichiers.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**Combinaison**
</dt> <dd>

Identificateur de fichier.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

Heure du dernier accès.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

Heure de la dernière modification.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

Heure de la dernière modification.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

Structure **d' \_ \_ attributs de fichier NFS** .

> [!Note]  
> Pour obtenir une description plus détaillée des membres de cette structure, consultez la structure **fattr3** dans la spécification du protocole NFS version 3 (telle que définie dans la [norme RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**
</dt> <dd>

Spécifie si la connexion sur laquelle le descripteur du partage NFS a été créé se trouve sur le protocole NFS version 2 ou NFS version 3.



| Valeur                            | Description              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS version 2<br/> |
| <span id="3"></span>1,3<br/> | NFS version 3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>    |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>         |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
