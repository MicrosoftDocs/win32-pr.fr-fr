---
description: La \_ classe WMI Win32 SerialPortConfiguration représente les paramètres de transmission de données sur un port série Windows. Cela comprend les configurations permettant d’établir une connexion et une vérification des erreurs.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Classe Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950449"
---
# <a name="win32_serialportconfiguration-class"></a>\_Classe SerialPortConfiguration Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ SerialPortConfiguration** représente les paramètres de transmission de données sur un port série Windows. Cela comprend les configurations permettant d’établir une connexion et une vérification des erreurs.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SerialPortConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SerialPortConfiguration** a ces propriétés.

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")
</dt> </dl>

Si la **valeur est true**, les opérations de lecture et d’écriture sont terminées si une erreur se produit. Si la **valeur est true**, le pilote met fin à toutes les opérations de lecture et d’écriture avec un état d’erreur si une erreur se produit. Le pilote n’accepte aucune autre opération de communication tant que l’application n’a pas confirmé l’erreur.

</dd> <dt>

**BaudRate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| structures de communication win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| baudrate »)
</dt> </dl>

Vitesse en bauds (bits par seconde) à laquelle l’appareil de communication fonctionne.

Exemple : 9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

Si la **valeur est true**, les transferts de données en mode binaire sont activés pour le port série. Les systèmes informatiques qui exécutent Windows autorisent uniquement les transferts binaires via les ports série. cette valeur est donc toujours **true**.

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| , octets)
</dt> </dl>

Nombre de bits transmis et reçus pour chaque octet de données pour le port série Windows. Le nombre peut varier selon les bits de contrôle et de correction d’erreur, tels que les bits de parité.

Exemple : 8

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")
</dt> </dl>

Si la **valeur est true**, les transmissions de données continuent lorsque la mémoire tampon d’entrée se trouve dans **XOffXMitThreshold** octets de plein et que le pilote a transmis la valeur **XOffChararcter** pour arrêter la réception d’octets. Si la valeur est **false**, la transmission ne continue pas tant que la mémoire tampon d’entrée ne se trouve pas dans **XOnXMitThreshold** octets de vide et que le pilote a transmis la valeur **XOnCharacter** pour reprendre la réception.

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")
</dt> </dl>

Si la **valeur est true**, le signal CTS (Clear to Send) est vérifié avant de transmettre les données. CTS signale que les deux appareils sur la connexion série sont prêts à transférer des données. La transmission de données est suspendue jusqu’à ce que le signal CTS soit donné.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DiscardNULLBytes**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")
</dt> </dl>

Si la **valeur est true**, les octets **nuls** (caractères) sont ignorés lorsqu’ils sont reçus.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")
</dt> </dl>

Si la **valeur est true**, le contrôle de flux de données est activé lorsqu’il existe une condition de jeu de données prêt (DSR). DSR signale que la connexion a été établie par les appareils sur la connexion série. La transmission des données DSR est suspendue jusqu’à ce que le signal DSR soit donné.

</dd> <dt>

**Sensibilité DSR**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")
</dt> </dl>

Si la **valeur est true**, le pilote de communication est sensible à l’état du signal DSR. Le pilote ignore les octets reçus, sauf si la ligne d’entrée du modem DSR est élevée.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")
</dt> </dl>

Utilisation du contrôle de déroulement DTR (Data Terminal Ready) après l’établissement d’une connexion.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Activer** (« activer »)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Désactiver** (« désactiver »)


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Protocole de transfert** (« négociation »)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caractère EOF**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")
</dt> </dl>

Valeur du caractère utilisé pour signaler la fin des données.

Exemple : ^ Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Valeur du caractère utilisé pour remplacer les octets reçus avec une erreur de parité.

Exemple : ^ C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")
</dt> </dl>

Si la valeur est **true**, les octets reçus avec des erreurs de parité sont remplacés par la valeur **ErrorReplaceCharacter** . Les caractères avec des erreurs de parité sont remplacés uniquement si cette propriété a la **valeur true** et que la parité est activée.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")
</dt> </dl>

Valeur du caractère de contrôle utilisé pour signaler un événement, telle que la fin du fichier.

Exemple : ^ e

</dd> <dt>

**IsBusy**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| fichier functions \| CreateFile")
</dt> </dl>

Si la **valeur est true**, le port série est occupé.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Nom du port série Windows.

Exemple : « COM1 »

</dd> <dt>

**Parité**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| structures de communication win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parity »)
</dt> </dl>

Méthode de contrôle de parité à utiliser. La parité est utilisée comme une technique de vérification des erreurs où un bit de parité supplémentaire est inclus avec chaque unité de données. Le récepteur peut ensuite vérifier la validité des données en comptant les bits qui sont définis.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (« aucun »)


</dt> <dd>

Vérification de la parité non utilisée.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Impair** (« impair »)


</dt> <dd>

Définit le bit de parité afin que le nombre de bits défini soit un nombre impair.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Même** (« pair »)


</dt> <dd>

Définit le bit de parité afin que le nombre de bits défini soit un nombre pair.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** (« Mark »)


</dt> <dd>

Laisse le bit de parité avec la valeur 1.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Espace** (« Space »)


</dt> <dd>

Laisse le bit de parité défini sur 0 (zéro).

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")
</dt> </dl>

Si la **valeur est true**, le contrôle de parité est activé.

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contrôle de flow de demande d’envoi (RTS). RTS est utilisé pour signaler que les données sont disponibles pour la transmission.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Activer** (« activer »)


</dt> <dd>

RTS est conservé pour la session de transfert de données.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (« désactiver »)


</dt> <dd>

RTS est ignoré après la réception du premier signal RTS.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Protocole de transfert** (« négociation »)


</dt> <dd>

RTS est désactivé si la mémoire tampon de transmission est pleine de plus de trois quarts et que RTS est activé lorsque la mémoire tampon est inférieure à une moitié pleine.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Activer/désactiver** (« bascule »)


</dt> <dd>

RTS est activé si des données sont mises en mémoire tampon pour la transmission.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**Bits d'arrêt**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| arrêt")
</dt> </dl>

Nombre de bits d’arrêt à utiliser. Les bits d’arrêt séparent chaque unité de données sur une connexion série asynchrone. Ils sont également envoyés en continu quand aucune donnée n’est disponible pour la transmission.

<dt>

<span id="1"></span>

**1** (« 1 »)


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1,5** ("1,5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (« 2 »)


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Valeur du caractère XOFF pour la transmission et la réception. XOFF est un contrôle logiciel permettant d’arrêter la transmission de données (alors que RTS et CTS sont des contrôles matériels). XON reprend la transmission.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")
</dt> </dl>

Nombre maximal d’octets autorisés dans la mémoire tampon d’entrée avant l’envoi du caractère XOFF.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")
</dt> </dl>

Valeur du caractère XON pour la transmission et la réception. XON est un contrôle logiciel pour reprendre la transmission de données (alors que RTS et CTS sont des contrôles matériels). XOFF arrête la transmission.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")
</dt> </dl>

Nombre minimal d’octets autorisés dans la mémoire tampon d’entrée avant l’envoi du caractère XON. Cette propriété fonctionne conjointement avec **XOffXMitThreshold** pour réguler la vitesse à laquelle les données sont transférées.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")
</dt> </dl>

Si la **valeur est true**, le contrôle de workflow XON/XOFF est utilisé lors de la réception. Si la valeur est **true**, la valeur **XOffCharacter** est envoyée lorsque la mémoire tampon d’entrée se trouve dans **XOffXMitThreshold** octets de plein, et la valeur **XOnCharacter** est envoyée lorsque la mémoire tampon d’entrée est vide dans **XOnXMitThreshold** octets.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

FALSE

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

TRUE

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")
</dt> </dl>

Le **XOnXOffOutFlowControl** spécifie si le contrôle de Flow Xon ou XOFF est utilisé lors de la transmission. Si la valeur est **true**, la transmission s’arrête lorsque la valeur **XOffCharacter** est reçue et redémarre lorsque la valeur **XOnCharacter** est reçue.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SerialPortConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
