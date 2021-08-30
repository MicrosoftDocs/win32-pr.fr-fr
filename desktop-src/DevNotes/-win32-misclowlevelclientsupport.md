---
description: cette rubrique contient des informations sur les api de bas niveau utilisées par l’infrastructure cliente Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Prise en charge des clients de Low-Level divers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffc5d32588089d3300ef59af17fe7ce2a0d0e99
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470176"
---
# <a name="miscellaneous-low-level-client-support"></a>Prise en charge des clients de Low-Level divers

cette rubrique contient des informations sur les api de bas niveau utilisées par l’infrastructure cliente Windows.

### <a name="functions"></a>Fonctions




| Rubrique | Contenu | 
|-------|----------|
| <a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a> | La fonction _lclose ferme le fichier spécifié afin qu’il ne soit plus disponible pour la lecture ou l’écriture. Cette fonction est fournie à des fins de compatibilité avec les versions 16 bits de Windows. Les applications Win32 doivent utiliser la fonction CloseHandle.<br /> | 
| <a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a> | La fonction _lopen ouvre un fichier existant et définit le pointeur de fichier au début du fichier. Cette fonction est fournie à des fins de compatibilité avec les versions 16 bits de Windows. Les applications Win32 doivent utiliser la fonction CreateFile. <br /> | 
| <a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a> | La fonction _lread lit les données du fichier spécifié. Cette fonction est fournie à des fins de compatibilité avec les versions 16 bits de Windows. Les applications Win32 doivent utiliser la fonction ReadFile. <br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a> | Retourne une valeur indiquant si les codecs DVD sont activés sur l’appareil actuel.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a> | Désactive la fonctionnalité de dédoublement de fenêtre pour le processus de l’interface graphique utilisateur appelant. le dédoublement de fenêtre est une fonctionnalité du gestionnaire de Windows qui permet à l’utilisateur de réduire, déplacer ou fermer la fenêtre principale d’une application qui ne répond pas.<br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a> | Retourne la liste des propriétés de tous les codecs multimédias installés sur le système qui répondent aux critères spécifiés.<br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a> | Crée une fabrique de communication pour l’inscription d’une extension de média.<br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a> | Crée une instance d’une classe dans un package d’application. <br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a> | Obtient une valeur indiquant si le comportement du média associé au GUID spécifié est activé.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> | Action déconseillée. Cette fonction est utilisée pour fermer le handle spécifié. <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> est remplacé par <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> | Action déconseillée. Génère des descripteurs pour la ou les mémoires tampons fournies et transmet les données non typées au pilote de périphérique associé au descripteur de fichier. <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> est remplacé par <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> | Action déconseillée. Attend que l’objet spécifié atteigne un état de <code>signaled</code> . <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> est remplacé par <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> | Convertit la chaîne source ANSI spécifiée en chaîne Unicode. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a> | Convertit une chaîne de caractères en entier.<br /> | 
| <a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a> | Initialise la mémoire tampon fournie avec une représentation sous forme de chaîne du SID de l’utilisateur actuel. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a> | Libère la mémoire tampon de chaîne allouée par <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a> | Libère la mémoire tampon de chaîne allouée par <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a> | Libère la mémoire tampon de chaîne allouée par <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> ou par <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a> | Initialise une chaîne comptée. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a> | Initialise une chaîne Unicode comptée. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a> | Convertit la chaîne source Unicode spécifiée en chaîne ANSI. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a> | Cette fonction convertit la chaîne source Unicode spécifiée en une chaîne OEM. La traduction est effectuée par rapport à la page de codes OEM (OCP). <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a> | Détermine le nombre d’octets nécessaires pour représenter une chaîne Unicode sous la forme d’une chaîne ANSI.<br /> | 
| <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> | La fonction <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> traduit la chaîne Unicode spécifiée en une nouvelle chaîne de caractères, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.<br /> | 
| <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> | La fonction <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> traduit la chaîne source spécifiée en chaîne Unicode, à l’aide de la page de codes UTF-8.<br /> | 
| <a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a> | Spécifie une action ou un traitement pour l’éditeur de méthode d’entrée (IME) via une sous-fonction spécifiée.<blockquote>[!Note]<br />Cette fonction est obsolète et ne doit pas être utilisée.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a> | Active ou désactive temporairement un IME et, en même temps, active ou désactive l’affichage de toutes les fenêtres détenues par l’IME.<blockquote>[!Note]<br />Cette fonction est obsolète et ne doit pas être utilisée.</blockquote><br /><br /> | 




 

### <a name="structures"></a>Structures



| Rubrique                                 | Contenu                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMESTRUCT**](/windows/win32/api/ime/ns-ime-imestruct) | Utilisé par [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) pour spécifier la sous-fonction à exécuter dans le message IME et ses paramètres. Cette structure est également utilisée pour recevoir des valeurs de retour de ces sous-fonctions.<br/> |
| [**CHAÎNE**](/windows/desktop/api/Winternl/ns-winternl-string)       | Cette structure est utilisée avec la fonction [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) . <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Routines du compilateur



| Rubrique                                                             | Contenu                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_\_Routine de gestionnaire spécifique à C \_**](--c-specific-handler2.md) | Le [**\_ \_ \_ \_ gestionnaire spécifique à c**](--c-specific-handler2.md) est une routine d’assistance pour le compilateur c.<br/> |
| [\_Routine alldiv](-win32-alldiv.md)                             | la [ \_ routine alldiv](-win32-alldiv.md) est une routine d’assistance pour le compilateur C.<br/>                     |
| [\_allmul](-win32-allmul.md) | Multiplie deux **LongLong** ou **ULONGLONG**. |
| [\_aulldiv](-win32-aulldiv.md) | Divise deux entiers **ULONGLONG** . |
| [\_Routine chkstk](-win32-chkstk.md)                             | la [ \_ routine chkstk](-win32-chkstk.md) est une routine d’assistance pour le compilateur C.<br/>                     |
