## Pessoa
- CPF
- Nome
- End_CEP
- End_Bairro
- End_Rua

## Telefone
- CPF
- Telefone

**Chaves Estrangeiras**
- CPF → Pessoa(CPF)

## Cliente
- CPF

**Chaves Estrangeiras**
- CPF → Pessoa(CPF)

## Estacionamento
- Endereço
- Capacidade

## Funcionário
- CPF
- Matrícula
- CPF_Chefe
- Endereço_estacionamento

**Chaves Estrangeiras**
- CPF → Pessoa(CPF)
- CPF_Chefe → Funcionário(CPF)
- Endereço_estacionamento → Estacionamento(Endereço)

## Veículo
- Placa
- Modelo

## Vaga
- Endereço_estacionamento
- Número

**Chaves Estrangeiras**
- Endereço_estacionamento → Estacionamento(Endereço)

## Reserva
- CPF_Cliente
- Placa_veiculo
- Endereço_estacionamento
- Número
- Valor
- Hora/Data

**Chaves Estrangeiras**
- CPF_Cliente → Cliente(CPF)
- Placa_veiculo → Veículo(Placa)
- Endereço_estacionamento, Número → Vaga(Endereço_estacionamento, Número)

## Cupom
- ID
- Valor
- CPF_Cliente
- Placa_veiculo

**Chaves Estrangeiras**
- CPF_Cliente, Placa_veiculo → Reserva(CPF_Cliente, Placa_veiculo)

## Possui
- CPF_cliente
- Placa_veiculo

**Chaves Estrangeiras**
- CPF_cliente → Cliente(CPF)
- Placa_veiculo → Veículo(Placa)
