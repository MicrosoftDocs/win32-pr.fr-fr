---
title: Commande MCI_SYSINFO (mmsystem. h)
description: La \_ commande MCI sysinfo récupère des informations sur les périphériques MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- commande MCI_SYSINFO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195080"
---
# <a name="mci_sysinfo-command"></a>\_Commande MCI sysinfo

La \_ commande MCI sysinfo récupère des informations sur les périphériques MCI. MCI prend en charge cette commande directement au lieu de la transmettre à l’appareil. Toute application MCI peut utiliser cette commande. Les informations de chaîne sont retournées dans la mémoire tampon fournie par l’application vers laquelle pointe le membre **lpstrReturn** de la structure identifiée par *lpSysInfo*. Les informations numériques sont retournées sous la forme d’une valeur **DWORD** placée dans la mémoire tampon fournie par l’application. Le membre **dwRetSize** spécifie la longueur de la mémoire tampon.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificateur de l’appareil MCI qui doit recevoir le message de commande.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Un ou plusieurs des indicateurs standard et spécifiques à la commande suivants :

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>\_INSTALLNAME MCI sysinfo \_
</dt> <dd>

Obtient le nom (indiqué dans le registre ou le fichier SYSTEM.INI) utilisé pour installer l’appareil.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_nom MCI sysinfo \_
</dt> <dd>

Obtient un nom de périphérique correspondant au numéro d’appareil spécifié dans le membre **dwNumber** de la structure identifiée par **lpSysInfo**. Si l' \_ \_ indicateur d’ouverture MCI sysinfo est défini, MCI retourne les noms des appareils ouverts.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ sysinfo \_ ouvert
</dt> <dd>

Obtient la quantité ou le nom des appareils ouverts.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_quantité MCI sysinfo \_
</dt> <dd>

Obtient le nombre d’appareils du type spécifié qui sont répertoriés dans le registre ou la \[ section MCI \] du fichier SYSTEM.INI. Si l' \_ \_ indicateur d’ouverture MCI sysinfo est défini, le nombre d’appareils ouverts est retourné.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

Pointeur vers une structure de valeur [**MCI \_ sysinfo \_**](mci-sysinfo-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Le membre **wDeviceType** de la structure identifiée par *lpSysInfo* est utilisé pour indiquer le type d’appareil de la requête. Si le paramètre *wDeviceID* est défini sur MCI \_ All \_ Device \_ ID, il remplace la valeur de **wDeviceType**. Pour obtenir la liste des types d’appareils, consultez [types d’appareils MCI](mci-device-types.md).

Les valeurs de retour de type entier sont des valeurs **DWORD** retournées dans la mémoire tampon vers laquelle pointe le membre **lpstrReturn** de la structure identifiée par *lpSysInfo*.

Les valeurs de retour de chaîne sont des chaînes terminées par le caractère null retournées dans la mémoire tampon vers laquelle pointe le membre **lpstrReturn** de la structure identifiée par *lpSysInfo*.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 

