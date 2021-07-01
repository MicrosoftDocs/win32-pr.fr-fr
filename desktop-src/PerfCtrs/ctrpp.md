---
description: L’outil CTRPP est un pré-processeur qui analyse et valide votre manifeste de compteurs.
ms.assetid: 3939f6a1-0a94-429d-a71e-b37f045fea13
title: CTRPP
ms.topic: reference
ms.date: 08/17/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- CTRPP
api_type:
- NA
api_location: ''
ms.openlocfilehash: eacfbb83abd56becc579c6b9bbaedacda96f94b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119104"
---
# <a name="ctrpp"></a>CTRPP

L’outil CTRPP est un pré-processeur qui analyse et valide le manifeste pour votre fournisseur v2. L’outil génère des `.rc` ressources avec les chaînes requises par les consommateurs de votre fournisseur et génère un `.h` en-tête avec le code que vous utilisez pour fournir vos données de compteur. Vous devez exécuter l’outil CTRPP pendant la génération de votre fournisseur. Vous devez utiliser le code généré comme point de départ lors du développement de votre fournisseur au lieu d’essayer de générer ce code vous-même.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Arguments

|Option              |Description
|--------------------|-----------
|*FichierEntrée*         |**Obligatoire :** Spécifie le nom du `.man` fichier (manifeste XML) qui définit vos compteurs.
|**-o** *CodeFile*   |**Obligatoire :** Spécifie le nom du `.h` fichier de code à générer par ctrpp. Ce fichier contient des fonctions d’assistance inline C/C++ qui simplifient l’initialisation et la désinitialisation de votre fournisseur.
|**-RC** *rcFile*    |**Obligatoire :** Spécifie le nom du `.rc` fichier de ressources à générer par ctrpp. Ce fichier contient la table de chaînes du fournisseur.
|**-ch** *symFile*   |Spécifie le nom du fichier de symboles facultatifs `.h` à générer par ctrpp. Ce fichier contient des symboles C/C++ pour les noms et les GUID de chaque CounterSet dans le fournisseur.
|**-** *préfixe* préfixe|Spécifie le préfixe à utiliser pour les variables et les fonctions définies dans le fichier d’en-tête généré.
|**-NotificationCallback**|Modifie la signature par défaut de la fonction [**CounterInitialize**](counterinitialize.md) pour inclure des paramètres pour la spécification du nom des fonctions de rappel [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest), [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)et [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Cet argument a le même effet que l’inclusion `callback` de l’attribut dans l’élément [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) .
|**-migrer** *outputfile*|Au lieu de générer et de créer des `.h` `.rc` fichiers, met à niveau le manifeste *FichierEntrée* vers la dernière version et l’enregistre dans *FichierSortie*. Ce commutateur ne peut pas être utilisé avec d’autres commutateurs. Utilisation : `CTRPP -migrate NewFile.man OldFile.man`
|**-Incompatibilité**     |**Déconseillé :** La prise en charge des fournisseurs en mode noyau a été ajoutée dans Windows 7. Par défaut, le code généré par CTRPP pour les fournisseurs en mode noyau est incompatible avec les versions antérieures de Windows (le pilote ne peut pas se charger en raison d’API manquantes `Pcw***` ). Défini `-BackCompat` pour activer la compatibilité avec les versions antérieures de Windows. Le pilote chargera dynamiquement les API nécessaires et le code généré désactivera silencieusement le fournisseur si les API ne sont pas disponibles.
|**-MemoryRoutines** |**Déconseillé :** En cas d’utilisation avec le `-Legacy` commutateur, comprend des modèles pour les routines de mémoire dans le code généré. Sinon, cet argument a le même effet que le `-NotificationCallback` commutateur.
|**-Hérité**         |**Déconseillé :** Génère `*.h` des `*.c` fichiers,, `*.rc` et `*_r.h` à l’aide des modèles de code Windows Vista (génère PerfAutoInitialize et PerfAutoCleanup au lieu de CounterInitialize et CounterCleanup). Ce commutateur peut être utilisé avec **-MemoryRoutines** et **-NotificationCallback** , mais il ne peut pas être utilisé avec d’autres commutateurs. N’utilisez pas les commutateurs **-o** ou **-RC** avec ce commutateur. Les fichiers générés sont nommés en fonction du nom du manifeste et sont écrits dans le répertoire qui contenait le manifeste. Utilisation : `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Remarques

L’outil CTRPP génère un fichier de `.h` code, un `.rc` fichier de ressources et, éventuellement, génère un `.h` fichier de symboles.

### <a name="using-the-generated-resource-file"></a>Utilisation du fichier de ressources généré

L’outil CTRPP génère un `.rc` fichier de ressources qui contient les chaînes localisables nécessaires aux consommateurs du countersets du fournisseur.

> [!IMPORTANT]
> Les ressources de ce fichier doivent être incluses dans votre binaire de fournisseur et le chemin d’accès complet au fichier binaire du fournisseur doit être inscrit pendant l’installation du manifeste de votre fournisseur. Les consommateurs qui ne parviennent pas à localiser et à charger les ressources ne pourront pas utiliser les countersets de votre fournisseur.

Les ressources de type chaîne doivent être gérées comme suit :

- Le développeur modifie le fichier manifeste du fournisseur ( `.man` ) afin de définir l' `applicationIdentity` attribut du fournisseur sur le nom d’un fournisseur (.DLL, .SYS ou .EXE) qui contiendra les ressources de type chaîne pour le fournisseur et sera installé dans le cadre du composant fournisseur.
- L’outil CTRPP lit le manifeste du fournisseur et génère un `.rc` fichier.
- L’outil [RC (compilateur de ressources)](../menurc/resource-compiler.md) compile les données du fichier généré par ctrpp `.rc` pour générer un `.res` fichier contenant les ressources binaires. Pour ce faire, vous pouvez compiler directement le fichier généré par CTRPP `.rc` ou en compilant un autre `.rc` fichier qui comprend le fichier généré par ctrpp `.rc` via une `#include` directive.
- L’éditeur de liens incorpore les données du fichier généré par RC `.res` dans le binaire du fournisseur.
- Pendant l’installation, le fichier binaire du fournisseur est copié sur le système de l’utilisateur et le manifeste du fournisseur est enregistré à l’aide de l' [outil lodctr](/windows-server/administration/windows-commands/lodctr). L’outil lodctr convertit l' `applicationIdentity` attribut du manifeste du fournisseur en chemin d’accès complet et enregistre le chemin d’accès complet au fichier binaire du fournisseur dans le registre.
  - Si le fichier binaire du fournisseur se trouve dans le même répertoire que le manifeste, utilisez : `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr associe le chemin d’accès du manifeste spécifié à l’attribut du manifeste `applicationIdentity` pour former le chemin d’accès complet.
  - Sinon, utilisez `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr associe le chemin d’accès binaire spécifié à l' `applicationIdentity` attribut du manifeste pour former le chemin d’accès complet.
  - À des fins de diagnostic, vous pouvez inspecter le chemin d’accès complet enregistré en vérifiant la `ApplicationIdentity` valeur de la clé de Registre `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Si le fichier binaire utilise MUI pour la localisation, veillez à copier le fichier MUI avec le fichier binaire.
- Pendant la collection CounterSet, le consommateur utilise le chemin d’accès complet enregistré au fichier binaire du fournisseur pour rechercher et charger les chaînes nécessaires à partir des ressources du binaire du fournisseur.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Utilisation du fichier de code généré dans un fournisseur en mode utilisateur

L’outil CTRPP génère un `.h` fichier de code C/C++. Si l’attribut du manifeste du fournisseur `providerType` a la valeur `userMode` , le fichier de code généré contient les définitions suivantes qui sont utiles pour le codage d’un fournisseur en mode utilisateur :

- Une fonction d’initialisation du fournisseur nommée [ * **préfixe * CounterInitialize**](counterinitialize.md).
- Une fonction de nettoyage du fournisseur nommée [ * **préfixe * CounterCleanup**](countercleanup.md).
- Variable globale ***Provider** _ qui stocke le handle du fournisseur ouvert par la fonction _ *_prefix_CounterInitialize**. Le nom de la variable est la valeur de l' `symbol` attribut de l' `provider` élément dans le manifeste. Cette variable doit être utilisée dans les appels à `PerfCreateInstance` , `PerfDeleteInstance` et à d’autres API pour contrôler les données de votre fournisseur.
- Pour chaque CounterSet, une variable **GUID * CounterSet *** globale avec le GUID du CounterSet. Le nom de la variable est la valeur de l’attribut de l' `counterSet` élément `symbol` plus le suffixe « GUID », par exemple `MyCounterSetGUID` . Cette variable doit être utilisée dans les appels à `PerfCreateInstance` , `PerfDeleteInstance` et à d’autres API pour contrôler les données de votre fournisseur.
- Pour chaque compteur, une macro de ***compteur*** avec la valeur du compteur `id` . Le nom de la macro est la valeur de l’attribut de l' `counter` élément `symbol` . Cette macro doit être utilisée dans les appels à `PerfSetCounterRefValue` , `PerfSetULongLongCounterValue` et à d’autres API pour définir les données de votre fournisseur.

Dans les noms de fonction, ***prefix*** fait référence à la valeur du `-prefix` paramètre de ligne de commande. Si le `-prefix` paramètre n’est pas utilisé, les fonctions sont nommées `CounterInitialize` et `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Utilisation du fichier de code généré dans un fournisseur en mode noyau

L’outil CTRPP génère un `.h` fichier de code C/C++. Si l’attribut du manifeste du fournisseur `providerType` a la valeur `kernelMode` , le fichier de code généré contient les définitions suivantes qui sont utiles pour coder les countersets d’un fournisseur en mode noyau :

- Une fonction d’initialisation CounterSet nommée <b> *prefix* Register *CounterSet*</b>. Cette fonction remplit une structure [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) , puis appelle [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister), en plaçant le handle d’inscription du CounterSet résultant dans la variable globale ***CounterSet*** .
- Une fonction de nettoyage du <b> *CounterSet nommée* Unregister *CounterSet*</b>. Cette fonction appelle [PcwUnregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) sur le handle d’inscription du CounterSet dans la variable globale ***CounterSet*** .
- Une fonction de création d’instance nommée <b> *prefix* Create *CounterSet*</b>. Cette fonction remplit un tableau de structures [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) , puis appelle [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) à l’aide du handle d’inscription du CounterSet dans la variable globale ***CounterSet*** .
- Une fonction de nettoyage d’instance nommée « <b> *préfixe*», fermer *CounterSet*</b>. Cette fonction appelle [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance).
- Une fonction de création de rapports d’instance nommée <b> *prefix* Add *CounterSet*</b> à utiliser à partir de la fonction de rappel du CounterSet. Cette fonction remplit un tableau de structures [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) , puis appelle [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **SDK Windows 20H1 et versions ultérieures :** Une fonction d’initialisation RegInfo nommée <b> *prefix* InitRegistrationInformation *CounterSet*</b> pour une utilisation dans des scénarios avancés. Cette fonction remplit une structure [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) . Cette fonction peut être utilisée dans les cas où le <b>Registre de *préfixe* généré *CounterSet*</b> ne répond pas à vos besoins, par exemple lorsque vous souhaitez personnaliser les valeurs dans la structure RegInfo ou lorsque vous souhaitez stocker le handle retourné dans une autre variable.

Dans les noms de fonction, ***prefix*** fait référence à la valeur du `-prefix` paramètre de ligne de commande. Si le `-prefix` paramètre n’est pas utilisé, les fonctions n’ont pas de préfixe.

> [!NOTE]
> La fonction <b>Add *CounterSet* de *préfixe*</b> générée est utilisée quand vous avez un rappel de CounterSet. Le <b> *préfixe* généré Create *CounterSet*</b> et le <b> *préfixe* de la fonction *CounterSet*</b> sont utilisés lorsque vous n’avez pas de rappel CounterSet.

### <a name="using-the-generated-symbol-file"></a>Utilisation du fichier de symboles généré

Si le paramètre **-ch** est spécifié sur la ligne de commande, l’outil ctrpp génère un `.h` fichier de symboles. Ce fichier contient les symboles C/C++ pour les noms et les GUID de chaque CounterSet dans le fournisseur. Les symboles peuvent être utilisés lors de l’écriture de programmes codés en dur pour consommer les données de ce CounterSet à l’aide des [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Spécifications

| Condition requise             | Value |
|-------------------------|-------|
| Client minimal pris en charge| Applications de \[ Bureau Windows Vista uniquement\]
| Serveur minimal pris en charge| Applications de bureau Windows Server 2008 \[ uniquement\]
