---
description: La liste suivante répertorie les qualificateurs utilisés pour définir les classes de fournisseur d’affichage.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualificateurs spécifiques au fournisseur de vues
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7890effa0e8edd07edbb9506f88a78ceffc65fcb8d19bf6c8bcf67860a677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130971"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Qualificateurs spécifiques au fournisseur de vues

La liste suivante répertorie les qualificateurs utilisés pour définir les classes de fournisseur d’affichage.

> [!Note]  
> La classe de fournisseur d’affichages prend en charge uniquement les noms NetBIOS lors de l’utilisation de références distantes. Si vous utilisez une adresse IP ou un nom DNS dans une référence distante, la connexion échoue avec une erreur 0x800706BA.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Directe**
</dt> <dd>

Type de données : **booléen**

Utilisé avec les propriétés d’association de vue pour empêcher le mappage des références d’association à une référence de vue.

L’exemple suivant définit la propriété **GroupComponent** comme une référence d’association qui n’est pas mappée dans la référence de vue.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**
</dt> <dd>

Type de données : **booléen**

Valeur par défaut pour une propriété de la classe d’affichage basée sur une propriété de classe source avec une valeur par défaut différente. La classe source sous-jacente est impliquée dans la vue.

Par exemple, la classe source [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) a une [](boolean.md) propriété booléenne **RunRepeatedly** qui indique si le travail doit être effectué périodiquement ou une seule fois. La valeur par défaut de **RunRepeatedly** n’est pas true pour **Win32 \_ ScheduledJob**, mais est true pour la classe d’affichage.


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**
</dt> <dd>

Type de données : **chaîne**

Définit comment les instances de classe source sont jointes dans les classes de vue de jointure. L’exemple suivant montre comment utiliser le qualificateur **JoinOn** pour joindre deux classes sources.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**
</dt> <dd>

Type de données : **tableau de chaînes**

Méthode source à exécuter pour la méthode d’affichage. Pour obtenir une syntaxe similaire, consultez [qualificateur PropertySources](propertysources-qualifier.md). La signature de la méthode doit correspondre exactement à la signature de la classe source. Copiez la signature de la méthode à partir du fichier MOF qui définit la classe source. L’exemple ci-dessous définit une méthode à partir de la méthode [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Ce qualificateur est valide uniquement lorsqu’il est utilisé avec les vues Union.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)
</dt> <dd>

Type de données : **chaîne**

Requête WQL pour filtrer les instances une fois qu’elles ont été jointes dans une classe join.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)
</dt> <dd>

Type de données : **tableau de chaînes**

Propriétés sources à partir desquelles une propriété de la classe d’affichage obtient des données.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**UE**
</dt> <dd>

Type de données : **booléen**

Indique si vous définissez une classe Union. Les vues Union contiennent des instances basées sur l’Union des instances source. Par exemple, vous pouvez déclarer ce qui suit :


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)
</dt> <dd>

Type de données : **tableau de chaînes**

Ensemble de requêtes de Langage de requêtes WMI (WQL) (WQL) qui définissent les instances source et les propriétés utilisées dans une classe d’affichage spécifique. La correspondance de position de tous les qualificateurs de tableau est importante.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)
</dt> <dd>

Type de données : **tableau de chaînes**

Espaces de noms où se trouvent les instances source.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

