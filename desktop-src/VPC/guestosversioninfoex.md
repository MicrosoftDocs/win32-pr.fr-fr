---
title: GUESTOSVERSIONINFOEX, structure (VPCCOMInterfaces. h)
description: Contient les informations de version du système d’exploitation pour le système d’exploitation invité.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX structure Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104278"
---
# <a name="guestosversioninfoex-structure"></a>GUESTOSVERSIONINFOEX, structure

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contient les informations de version du système d’exploitation pour le système d’exploitation invité.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwOSVersionInfoSize**
</dt> <dd>

Taille de cette structure de données, en octets. Affectez à ce membre la valeur `sizeof(GUESTOSVERSIONINFOEX)` .

</dd> <dt>

**dwMajorVersion**
</dt> <dd>

Numéro de version principale.

</dd> <dt>

**dwMinorVersion**
</dt> <dd>

Numéro de version secondaire.

</dd> <dt>

**dwBuildNumber**
</dt> <dd>

Numéro de build.

</dd> <dt>

**dwPlatformId**
</dt> <dd>

Plateforme du système d’exploitation. Ce membre peut être de la **\_ plateforme ver \_ Win32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Chaîne terminée par le caractère null, telle que « Service Pack 3 », qui indique le dernier Service Pack installé sur le système. Si aucun Service Pack n’a été installé, la chaîne est vide.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Numéro de version principale du dernier Service Pack installé.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

Numéro de version mineure du dernier Service Pack installé.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Masque de masque qui identifie les suites de produits disponibles sur le système. Ce membre peut être une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**Ver \_ SUITE \_ BackOffice**</dt> <dt>0x00000004</dt> </dl>                                            | Les composants Microsoft BackOffice sont installés.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**Ver \_ Panneau \_ de suite**</dt> <dt>0x00000400</dt> </dl>                                                           | Windows Server 2003, Web Edition est installé.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**Ver \_ SUITE de \_ \_ serveurs de calcul**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition est installé.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**Ver \_ SUITE \_ Datacenter**</dt> <dt>0x00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server est installé.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 entreprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server est installé. Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded est installé.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**Ver \_ 0x00000200 \_ personnel de suite**</dt> <dt></dt> </dl>                                                  | Windows Vista Édition familiale Premium, Windows Vista Édition familiale basique ou Windows XP Édition familiale est installé.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Bureau à distance est pris en charge, mais une seule session interactive est prise en charge. Cette valeur est définie, sauf si le système s’exécute en mode serveur d’applications.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**Ver \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server a été installé sur le système, mais il a peut-être été mis à niveau vers une autre version de Windows. Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**Ver \_ SUITE \_ \_ restreinte**</dt> <dt>0x00000020</dt> de la suite </dl> | Microsoft Small Business Server est installé avec la licence client restrictive en vigueur. Reportez-vous à la section Remarques pour plus d’informations sur cet indicateur de bit.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**Ver \_ 0x00002000 \_ \_ serveur de stockage**</dt> de la suite <dt></dt> </dl>                               | Windows Storage Server 2003 R2 ou Windows Storage Server 2003 est installé.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**Ver \_ \_Terminal de suite**</dt> <dt>0x00000010</dt> </dl>                                                  | Les services Terminal Server sont installés. Cette valeur est toujours définie.<br/> Si la valeur terminal de la **\_ suite \_ ver** est définie mais que la **suite de \_ \_ SINGLEUSERTS** de version n’est pas définie, le système s’exécute en mode serveur d’applications.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**Ver \_ SUITE \_ 0x00008000 \_ serveur**</dt> <dt></dt> </dl>                                              | Windows Server famille est installé.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Toutes les informations supplémentaires sur le système. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**Ver \_ \_ \_ Contrôleur de domaine NT**</dt> <dt>0x0000002</dt> </dl> | Le système est un contrôleur de domaine et le système d’exploitation est Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**Ver \_ 0x0000003 NT \_ Server**</dt> <dt></dt> </dl>                                   | Le système d’exploitation est Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.<br/> Notez qu’un serveur qui est également un contrôleur de domaine est signalé en tant que **\_ \_ \_ contrôleur de domaine NT**, pas **ver \_ NT \_ Server**.<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**Ver \_ \_Station de travail NT**</dt> <dt>0x0000001</dt> </dl>                    | Le système d’exploitation est Windows 7, Windows Vista, Windows XP ou Windows 2000 professionnel.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Réservé pour un usage futur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

