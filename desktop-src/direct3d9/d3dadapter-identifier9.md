---
description: Contient des informations identifiant l’adaptateur.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Structure D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: db4b25cb44b3b43b3b9754f241e2c505bdfedbc7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343394"
---
# <a name="d3dadapter_identifier9-structure"></a>D3DADAPTER \_ IDENTIFIER9, structure

Contient des informations identifiant l’adaptateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a>Membres

<dl> <dt>

**Driver**
</dt> <dd>

Type : **char**

</dd> <dd>

Utilisé pour la présentation à l’utilisateur. Cela ne doit pas être utilisé pour identifier des pilotes particuliers, car de nombreuses chaînes différentes peuvent être associées au même appareil et au même pilote de différents fournisseurs.

</dd> <dt>

**Description**
</dt> <dd>

Type : **char**

</dd> <dd>

Utilisé pour la présentation à l’utilisateur.

</dd> <dt>

**DeviceName**
</dt> <dd>

Type : **char**

</dd> <dd>

Nom de l’appareil pour GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identifiez la version du pilote Direct3D. Il est possible d’effectuer des comparaisons inférieur à et supérieur à sur la valeur de l’entier signé 64 bits. Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques. Au lieu de cela, vous devez utiliser DeviceIdentifier. Consultez la section Notes.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifiez la version du pilote Direct3D. Il est possible d’effectuer des comparaisons < et > sur la valeur de l’entier signé 64 bits. Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques. Au lieu de cela, vous devez utiliser DeviceIdentifier. Consultez la section Notes.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifiez la version du pilote Direct3D. Il est possible d’effectuer des comparaisons < et > sur la valeur de l’entier signé 64 bits. Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques. Au lieu de cela, vous devez utiliser DeviceIdentifier. Consultez la section Notes.

</dd> <dt>

**VendorId**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Peut être utilisé pour aider à identifier un jeu de processeurs particulier. Interrogez ce membre pour identifier le fabricant. La valeur peut être zéro si inconnu.

</dd> <dt>

**DeviceId**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Peut être utilisé pour aider à identifier un jeu de processeurs particulier. Interrogez ce membre pour identifier le type de processeur. La valeur peut être zéro si inconnu.

</dd> <dt>

**SubSysId**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Peut être utilisé pour aider à identifier un jeu de processeurs particulier. Interrogez ce membre pour identifier le sous-système, généralement le tableau particulier. La valeur peut être zéro si inconnu.

</dd> <dt>

**Faisant**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Peut être utilisé pour aider à identifier un jeu de processeurs particulier. Interrogez ce membre pour identifier le niveau de révision du jeu de processeurs. La valeur peut être zéro si inconnu.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Type : **[ **GUID**](guid.md)**

</dd> <dd>

Peut être interrogé pour vérifier les modifications apportées au pilote et au jeu de processeurs. Ce GUID est un identificateur unique pour le couple du pilote et du jeu de processeurs. Interrogez ce membre pour effectuer le suivi des modifications apportées au pilote et au jeu de processeurs afin de générer un nouveau profil pour le sous-système graphique. DeviceIdentifier peut également être utilisé pour identifier des pilotes problématiques particuliers.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Utilisé pour déterminer le niveau de validation WHQL (Windows Hardware Quality Labs) pour ce pilote et cette paire d’appareils. La valeur DWORD est une structure de date compressée qui définit la date de publication du test WHQL le plus récent passé par le pilote. Il est légal d’effectuer des opérations de < et de > sur cette valeur. L’exemple suivant illustre le format de date.



| Bits  |  Description                                             |
|-------|-----------------------------------------------|
| 31-16 | Année, un nombre décimal compris entre 1999 et plus. |
| 15-8  | Le mois, un nombre décimal compris entre 1 et 12.     |
| 7-0   | Le jour, un nombre décimal compris entre 1 et 31.       |



 

Les valeurs suivantes sont également utilisées.



| Valeur    |  Description                                                     |
|-----|-------------------------------------------------------|
| 0   | Non certifié.                                        |
| 1   | WHQL validée, mais aucune information de date n’est disponible. |



 

Différences entre Direct3D 9 et Direct3D 9Ex :

Pour les Direct3D9Ex s’exécutant sur Windows Vista, Windows Server 2008, Windows 7 et Windows Server 2008 R2 (ou plus le système d’exploitation actuel), [**IDirect3D9 :: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) retourne 1 pour le niveau WHQL sans vérifier l’état du pilote.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’exemple de pseudo-code suivant illustre le format de version encodé dans les membres DriverVersion, DriverVersionLowPart et DriverVersionHighPart.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Consultez le kit de développement Platform SDK pour plus d’informations sur la macro HIWORD, la macro LOWORD et la grande \_ structure d’entiers.

\_ \_ La chaîne d’identificateur de périphérique Max \_ est une constante avec la définition suivante.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



Les membres ID de périphérique, DeviceId, SubSysId et Revision peuvent être utilisés en tandem pour identifier des jeux de puces particuliers. Toutefois, utilisez ces membres avec précaution.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
