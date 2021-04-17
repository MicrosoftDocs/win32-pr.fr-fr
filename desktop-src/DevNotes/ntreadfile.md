---
description: Lit les données d’un fichier ouvert.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Fonction NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523175"
---
# <a name="ntreadfile-function"></a>NtReadFile fonction)

Lit les données d’un fichier ouvert.

Cette fonction est l’équivalent du mode utilisateur à la fonction [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentée dans le kit WDK (Windows Driver Kit).

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileHandle* \[ dans\]
</dt> <dd>

Handle de l’objet de fichier. Ce handle est créé par un appel réussi à [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) ou [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).

</dd> <dt>

*Événement* \[ dans, facultatif\]
</dt> <dd>

Éventuellement, un handle vers un objet d’événement à affecter à l’état signalé une fois l’opération de lecture terminée. Les pilotes de périphériques et intermédiaires doivent définir ce paramètre sur la **valeur null**.

</dd> <dt>

*ApcRoutine* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre est réservé. Les pilotes de périphériques et intermédiaires doivent définir ce pointeur sur la **valeur null**.

</dd> <dt>

*ApcContext* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre est réservé. Les pilotes de périphériques et intermédiaires doivent définir ce pointeur sur la **valeur null**.

</dd> <dt>

*IoStatusBlock* \[ à\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ bloc d’état d’e/s**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) qui reçoit l’état d’achèvement final et des informations sur l’opération de lecture demandée. Le membre d' **informations** reçoit le nombre d’octets réellement lus à partir du fichier.

</dd> <dt>

*Mémoire tampon* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant qui reçoit les données lues à partir du fichier.

</dd> <dt>

*Longueur* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe la *mémoire tampon*.

</dd> <dt>

*ByteOffset* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une variable qui spécifie l’offset d’octet de début dans le fichier où l’opération de lecture doit commencer. En cas de tentative de lecture au-delà de la fin du fichier, **NtReadFile** retourne une erreur.

Si l’appel à [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) a défini l’une des alertes d’e/s synchrones de fichier d’indicateurs *CreateOptions* ou de non-alerte d’e \_ \_ \_ \_ \_ /s synchrones \_ , le gestionnaire d’e/s conserve la position de fichier actuelle. Dans ce cas, l’appelant de **NtReadFile** peut spécifier que le décalage de position de fichier actuel soit utilisé à la place d’une valeur *ByteOffset* explicite. Cette spécification peut être effectuée à l’aide de l’une des méthodes suivantes :

-   Spécifiez un pointeur vers une valeur **\_ entière de type long** avec le membre **HighPart** défini sur-1 et le membre **LowPart** défini sur le fichier de valeurs défini par le système utiliser la position du \_ pointeur de \_ fichier \_ \_ .

-   Passer un pointeur **null** pour *ByteOffset*.

**NtReadFile** met à jour la position de fichier actuelle en ajoutant le nombre d’octets lus lorsqu’il termine l’opération de lecture, s’il utilise la position de fichier actuelle gérée par le gestionnaire d’e/s.

Même lorsque le gestionnaire d’e/s maintient la position de fichier actuelle, l’appelant peut réinitialiser cette position en passant une valeur *ByteOffset* explicite à **NtReadFile**. Cette opération change automatiquement la position du fichier actuel en cette valeur *ByteOffset* , exécute l’opération de lecture, puis met à jour la position en fonction du nombre d’octets réellement lus. Cette technique permet au service de recherche et de lecture atomiques de l’appelant.

</dd> <dt>

*Clé* \[ dans, facultatif\]
</dt> <dd>

Les pilotes de périphériques et intermédiaires doivent définir ce pointeur sur la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtReadFile** retourne l’état \_ Success ou le code d’erreur NTSTATUS approprié.

## <a name="remarks"></a>Notes

Les appelants de **NtReadFile** doivent avoir déjà appelé [**NTCREATEFILE**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) avec le fichier \_ Read \_ Data ou generic \_ value défini dans le paramètre *desiredAccess* .

Si l’appel précédent à [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) affecte au fichier \_ aucun \_ \_ indicateur de mise en mémoire tampon intermédiaire dans le paramètre *CreateOptions* la valeur **NtCreateFile**, les paramètres *Length* et *ByteOffset* à **NtReadFile** doivent être des multiples de la taille de secteur. Pour plus d’informations, consultez **NtCreateFile**.

**NtReadFile** commence à lire à partir du *ByteOffset* donné ou à la position actuelle du fichier dans la *mémoire tampon* donnée. Elle met fin à l’opération de lecture dans l’une des conditions suivantes :

-   La mémoire tampon est saturée, car le nombre d’octets spécifié par le paramètre de *longueur* a été lu. Par conséquent, aucune donnée ne peut être placée dans la mémoire tampon sans dépassement de capacité.

-   La fin du fichier est atteinte pendant l’opération de lecture, de sorte qu’il n’y a plus de données dans le fichier à transférer dans la mémoire tampon.

Si l’appelant a ouvert le fichier avec l’indicateur de synchronisation défini dans *desiredAccess*, le thread appelant peut se synchroniser avec l’achèvement de l’opération de lecture en attendant le handle de fichier, *FileHandle*. Le descripteur est signalé chaque fois qu’une opération d’e/s émise sur le descripteur est terminée. Toutefois, l’appelant ne doit pas attendre sur un handle qui a été ouvert pour l’accès synchrone aux fichiers (alerte e/s synchrone de fichier non- \_ \_ \_ alerte ou d' \_ \_ e/s synchrone de fichier \_ ). Dans ce cas, **NtReadFile** attend pour le compte de l’appelant et n’est pas retourné tant que l’opération de lecture n’est pas terminée. L’appelant peut attendre en toute sécurité le descripteur de fichier uniquement si les trois conditions suivantes sont remplies :

-   Le descripteur a été ouvert pour un accès asynchrone (autrement dit, aucun \_ \_ indicateur d’e/s synchrone de fichier \_  n’a été spécifié).

-   Le descripteur est utilisé pour une seule opération d’e/s à la fois.

-   **NtReadFile** a retourné l’état \_ en attente.

Un pilote doit appeler **NtReadFile** dans le contexte du processus système si l’une des conditions suivantes est remplie :

-   Le pilote a créé le descripteur de fichier qu’il transmet à **NtReadFile**.

-   **NtReadFile** informe le pilote d’achèvement des e/s au moyen d’un événement que le pilote a créé.

-   **NtReadFile** informe le pilote d’achèvement des e/s au moyen d’une routine de rappel APC que le pilote transmet à **NtReadFile**.

Les handles de fichiers et d’événements ne sont valides que dans le contexte de processus où les descripteurs sont créés. Par conséquent, pour éviter les brèches de sécurité, le pilote doit créer tout handle de fichier ou d’événement qu’il transmet à **NtReadFile** dans le contexte du processus système plutôt que dans le contexte du processus dans lequel se trouve le pilote.

De même, **NtReadFile** doit être appelé dans le contexte du processus système s’il notifie le pilote d’achèvement des e/s au moyen d’un APC, car les APC sont toujours déclenchés dans le contexte du thread qui émet la requête d’e/s. Si le pilote appelle **NtReadFile** dans le contexte d’un processus autre que celui du système, l’APC peut être retardé indéfiniment ou ne pas se déclencher du tout.

Pour plus d’informations sur l’utilisation des fichiers, consultez [utilisation de fichiers dans un pilote](/windows-hardware/drivers/kernel/using-files-in-a-driver).

Les appelants de **NtReadFile** doivent s’exécuter au niveau IRQL = passif \_ et les appels de fonction de [noyau spéciaux sont activés](/windows-hardware/drivers/kernel/disabling-apcs).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                    |
| Plateforme cible<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| En-tête<br/>                   | <dl> <dt>WDM. h (inclure WDM. h, Ntddk. h ou Ntifs. h)</dt> </dl>                   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll (mode utilisateur)</dt> </dl>                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**KeInitializeEvent**](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[**NtQueryInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[**NtSetInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[**NtWriteFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
