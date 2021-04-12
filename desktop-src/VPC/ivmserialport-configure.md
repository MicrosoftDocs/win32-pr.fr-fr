---
title: IVMSerialPort configure, méthode (VPCCOMInterfaces. h)
description: Configure le port série.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurer la méthode Virtual PC
- Configurer la méthode Virtual PC, interface IVMSerialPort
- IVMSerialPort interface Virtual PC, configurer la méthode
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032930"
---
# <a name="ivmserialportconfigure-method"></a>IVMSerialPort :: configure, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configure le port série.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*portType* \[ dans\]
</dt> <dd>

Type de port série. Pour obtenir la liste des valeurs, consultez [**VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*PortName* \[ dans\]
</dt> <dd>

Nom du port série. Par exemple, « COM1 » pour **vmSerialPort \_ appelait hostport**, « C : \\SerialPort.txt » pour **vmSerialPort \_ TextFile**, ou « \\ \\ *ServerName* \\ pipe \\ *pipeName*» pour **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ dans\]
</dt> <dd>

**True** si le port série de l’hôte doit être ouvert immédiatement au démarrage de l’ordinateur virtuel et **false** dans le cas contraire. Ignoré si *portType* n’est pas **vmSerialPort \_ appelait hostport**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Le paramètre *portType* n’est pas valide.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                      |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *PortName* a la **valeur null**.<br/>                                                                                  |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl>      | La mémoire disponible est insuffisante pour effectuer cette requête.<br/>                                                         |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *PortName* est trop long. Le chemin d’accès doit être inférieur à la **longueur maximale \_** (260) caractères.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *PortName* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).<br/>                                    |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *PortName* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                            | La configuration de cet ordinateur virtuel n’est pas valide.<br/>                                                               |
| <dl> <dt>**Ordinateur virtuel \_ E \_ pref \_ \_ valeur non conforme**</dt> <dt>0xA0040301</dt> </dl>                   | Le port spécifié est déjà utilisé.<br/>                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

