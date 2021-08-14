---
description: La classe singleton ScriptingStandardConsumerSetting fournit des données d’inscription communes à toutes les instances de la classe de consommateur standard ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: ScriptingStandardConsumerSetting, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: a69d30511d01fba2df39483d1f76616bfae7c92812ce75989fd0c23558558b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316203"
---
# <a name="scriptingstandardconsumersetting-class"></a>ScriptingStandardConsumerSetting, classe

La classe singleton **ScriptingStandardConsumerSetting** fournit des données d’inscription communes à toutes les instances de la classe de consommateur standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) . Une instance **ActiveScriptEventConsumer** utilise les propriétés **MaximumScripts** et **timeout** . Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>Membres

La classe **ScriptingStandardConsumerSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **ScriptingStandardConsumerSetting** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](standard-qualifiers.md) (64)
</dt> </dl>

Description succincte d’un objet d’une chaîne d’une ligne. Contient la chaîne **ScriptingStandardConsumerSetting** , car il s’agit d’une classe singleton.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle d’un objet.

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre maximal de scripts qui sont exécutés avant qu’un consommateur ne démarre une nouvelle instance. Pour éliminer les fuites de mémoire des scripts, arrêtez le consommateur régulièrement. La valeur par défaut est 300.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](standard-qualifiers.md) (256)
</dt> </dl>

Identificateur de l’objet de paramètre.

</dd> <dt>

**Délai d'expiration**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**unités**](standard-qualifiers.md) (« minutes »)
</dt> </dl>

Nombre maximal de minutes avant le démarrage d’une nouvelle instance par un consommateur. Si la valeur est 0 (zéro), la propriété **MaximumScripts** contrôle la durée de vie du consommateur. La plage valide pour le **délai d’attente** est comprise entre 0 et 71 000 et la valeur par défaut est 0 (zéro).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’instance unique de la classe **ScriptingStandardConsumerSetting** réside dans l' \\ espace de noms CIMV2 racine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | \\Abonnement racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Classes de consommateur standard](standard-consumer-classes.md)
</dt> <dt>

[Exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)
</dt> <dt>

[Création d’un consommateur logique](creating-a-logical-consumer.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

